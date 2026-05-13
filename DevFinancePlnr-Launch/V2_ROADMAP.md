# V2 Backend Phase Roadmap
**Developer Finance Plnr**

Items deferred from v1 (BYOK launch) to v2 (backend + Pro tier).

---

## Why a backend phase

V1 ships with BYOK (bring-your-own-key) for Anthropic + RentCast. That's friction-heavy
(30-50% drop-off at the API key step) but zero cost to operate.

V2 introduces a server proxy that holds your keys, charges users via IAP, and removes
the BYOK step. This becomes the **Pro tier upgrade story**.

---

## V2 Pro tier value prop

| Free (BYOK or skip) | Pro ($9.99/mo or $79/yr) |
|---|---|
| Bring your own Anthropic key for Helper | Unlimited Helper bot, no key needed |
| Bring your own RentCast key for Comps | Unlimited Comps, no key needed |
| Local-only saved deals | Cloud sync across devices |
| No support | Priority email support |

Conversion target: 2-5% free → paid (industry benchmark for niche SaaS).

---

## Build order

### Phase A — User Accounts (1-2 days)
- [ ] Add `expo-apple-authentication`
- [ ] Add `@react-native-google-signin/google-signin`
- [ ] Build sign-in screen (Apple required by App Store rules if any social login present)
- [ ] Add "Continue without account" path so app still works for free/local-only users
- [ ] Add user profile / sign-out in Settings

### Phase B — Backend (2-4 days)
- [ ] Choose host: **Cloudflare Workers** (free tier covers ~100K req/day) or **Vercel Edge** (free tier)
- [ ] Build endpoints:
  - `POST /api/helper` — proxy Claude with rate limiting
  - `POST /api/comps` — proxy RentCast with rate limiting
  - `GET /api/user` — fetch entitlements (Pro status)
- [ ] Auth middleware verifying Apple/Google JWT
- [ ] Per-user rate limits (tier-based)
- [ ] Request/response logging for billing reconciliation

### Phase C — IAP Wiring (1-2 days)
- [ ] Add `react-native-iap`
- [ ] Create products in App Store Connect:
  - `pro_monthly` — $9.99/mo auto-renewing
  - `pro_yearly` — $79/yr auto-renewing (advertise "Save 34%")
  - `pro_lifetime` — $199 one-time
- [ ] Same in Google Play Console
- [ ] Build paywall screen (clean upsell with feature list)
- [ ] Add "Restore purchases" button (Apple requirement)
- [ ] Receipt validation server-side (Apple/Google webhooks → backend updates user entitlements)

### Phase D — Cloud Sync (2-3 days)
- [ ] Backend storage (Cloudflare KV, Workers D1, or Vercel KV — all free tier)
- [ ] Sync endpoints for:
  - Saved deals (`saved_records_v1`)
  - DfD leads (`dfd_leads_v1`)
  - Cash buyers (`cash_buyers_v1`)
- [ ] Conflict resolution (last-write-wins acceptable for v1)
- [ ] Background sync on app foreground

### Phase E — Migrate Helper + Comps off BYOK (1 day)
- [ ] Replace direct API calls with calls to your backend proxy
- [ ] Hide BYOK setup in Settings (keep as advanced option for power users)
- [ ] Show "Pro" badge / paywall when free users hit limits

---

## Cost estimates at scale

Assuming Pro at $9.99/mo, average user: 50 helper sessions + 10 comp pulls / month.

| Users | Revenue/mo | API costs/mo | Net/mo |
|---|---|---|---|
| 100 paying | $999 | ~$50 (Anthropic) + $50 (RentCast) | ~$900 |
| 500 paying | $4,995 | ~$250 + $250 | ~$4,500 |
| 1,000 paying | $9,990 | ~$500 + $500 (or $50 unlimited rentcast tier) | ~$9,000 |

Anthropic Haiku 4.5: $1/$5 per million input/output tokens. Heavy use is ~$0.50/user/mo.
RentCast: free tier 50/mo, $0.10/call after, or $50/mo unlimited. At scale, switch to $50/mo unlimited.

---

## What stays BYOK forever (likely)

- Power users with their own API keys can opt OUT of Pro and still use bot/comps via BYOK.
- Keeps the door open for people who don't want a subscription but still want functionality.
- Settings should keep the "Add your own key" option as Advanced.

---

## Apple Compliance Notes

- **Subscriptions must use Apple IAP** — no Stripe redirect for digital goods on iOS.
- **Sign in with Apple required** if any social login is offered (App Store rule § 4.8).
- **Privacy Manifest** (PrivacyInfo.xcprivacy) required for iOS 17+ — declare data collection
  (none in v1; in v2: declare device identifiers used for backend account linking).
- **App Tracking Transparency** prompt — only needed if you use third-party tracking SDKs (we don't plan to).

---

## Estimated total time for v2

**~7-12 days of focused dev work** spread over 2-3 weeks. Best done after v1 has 50+ active
users and you can see which features get heaviest use (so you paywall the right things).

---

*Created: 2026-05-07*
*Last updated: 2026-05-07*
