# Privacy Policy
**Developer Finance Plnr**

**Effective Date:** [INSERT DATE]
**Last Updated:** [INSERT DATE]

---

> ⚠️ **TEMPLATE NOTICE — REPLACE BEFORE LAUNCH**
> This is a starter template. Before publishing to the App Store or Google Play, you MUST:
> 1. Replace [BRACKETED] placeholders with your actual info (name, contact email, etc.)
> 2. Have a licensed attorney review for your specific jurisdiction (especially for California CCPA/CPRA, EU GDPR, and Apple/Google compliance)
> 3. Host this at a public URL (e.g., GitHub Pages, your website) and link it from your App Store listing
>
> Free hosting options: GitHub Pages, Netlify, Cloudflare Pages, Termly.io (which can also generate a fully compliant version automatically).

---

## 1. Who We Are

This privacy policy describes how **[YOUR NAME or COMPANY LLC]** ("we," "us," "our") handles information when you use the **Developer Finance Plnr** mobile application (the "App").

**Contact:**
[YOUR EMAIL ADDRESS]
[YOUR MAILING ADDRESS — required for some jurisdictions]

---

## 2. The Short Version

- We don't have a server. We don't collect your data.
- Everything you enter (deals, budgets, contracts, addresses, your Anthropic API key, your saved records) stays **on your device only**.
- The App makes calls to public third-party APIs (Census, BLS, FBI, FRED, Yahoo Finance, Zippopotam.us, NETROnline, Anthropic) on your behalf. Those services have their own privacy policies.
- We do not use ads, trackers, or analytics.

---

## 3. What We Don't Do

- We do **not** require you to create an account.
- We do **not** collect your name, email, phone number, or contacts.
- We do **not** track your usage or behavior in the App.
- We do **not** sell, rent, or share any data — because we don't collect any.
- We do **not** include third-party advertising SDKs or tracking pixels.
- We do **not** access your photos, microphone, or contacts.

---

## 4. Information You Provide That Stays On Your Device

The App stores the following information **locally** on your phone using the operating system's secure storage (`AsyncStorage`):

- **Deal inputs** — purchase price, ARV, rehab cost, rental income, etc.
- **Rehab budget line items** — costs for demo, kitchen, baths, etc.
- **Saved deals & saved budgets** — when you tap "Save"
- **Contract field entries** — seller info, buyer info, property addresses (when generating contracts)
- **Your Anthropic API key** — if you set up the optional Rehab Helper bot
- **Chat history with the Helper bot** — recent conversation, capped at 50 messages
- **Cached data** — state-level real estate data is cached for 7 days for offline use

All of the above:
- Lives only on your device
- Is never transmitted to us (we have no servers to receive it)
- Is deleted when you uninstall the App

---

## 5. Third-Party Services The App Communicates With

The App connects to the following public services to provide its features. **We do not control these services. Your interaction with them is governed by their own privacy policies.**

| Service | Purpose | Information Sent |
|---|---|---|
| **U.S. Census Bureau API** | City population & autocomplete | City name, state code |
| **U.S. Bureau of Labor Statistics (BLS)** | State unemployment rate | State FIPS code |
| **FBI Crime Data API** | State violent crime stats | State code |
| **FRED (Federal Reserve)** | Mortgage rates, Treasury yields | None — public data feed |
| **Yahoo Finance** | Real estate stock prices | Ticker symbol |
| **Zippopotam.us** | ZIP → city/state lookup | 5-digit ZIP code |
| **NETROnline** | County records portal (link only) | None |
| **GitHub raw content** | Annual data refresh JSON | None |
| **Anthropic Claude API** *(optional, only if you set up the Helper bot)* | AI rehab/wholesale Q&A | Your chat messages + your API key |
| **Zillow / Redfin / Google** | Property lookup (opens external browser) | Address you enter (sent only when you tap the button) |

**Anthropic-specific note:** if you opt into the Helper bot, your messages and Anthropic API key are transmitted directly from your device to Anthropic's servers. We do not see, store, or relay your messages or key. See Anthropic's privacy policy at https://www.anthropic.com/legal/privacy.

---

## 6. Children's Privacy

The App is not directed at children under 13 and we do not knowingly collect any information from children. The App's content (real estate investing, contracts) is intended for adult users.

---

## 7. California (CCPA / CPRA) Notice

California residents have specific rights regarding personal information. Because we do not collect personal information, we do not sell or share personal information, and there is no personal information to access or delete on our servers (we have none). All data remains on your device. To delete data on your device, uninstall the App.

---

## 8. EU/UK Residents (GDPR)

We process no personal data within the meaning of GDPR. Local data on your device is fully under your control. The third-party APIs listed above are accessed by your device; their use is governed by each provider's own GDPR posture.

---

## 9. Data Security

Local data is protected by your device's operating system security (iOS Keychain / Android Keystore equivalents via `AsyncStorage`). We strongly recommend:
- Use a passcode/biometric on your phone
- Keep iOS or Android updated
- Don't jailbreak/root your device

We cannot recover data lost from device failure, theft, or uninstall. **There is no cloud backup of your saved deals or contracts** unless and until cloud sync is added in a future version (you will be notified before such a feature is enabled).

---

## 10. App Permissions

The App requests **no special permissions** beyond standard internet access (for the third-party APIs above). It does not request:
- Camera
- Microphone
- Contacts
- Location
- Photos / Files
- Push notifications
- Bluetooth

If a future version requires any of these, you will be asked at the time of the feature request and can decline.

---

## 11. In-App Purchases (When Added)

This version of the App is **free**. If we add paid features in the future:
- Purchases will be handled by **Apple App Store** or **Google Play Store** in-app purchase systems
- **We do not receive your payment card details** — those are handled by Apple/Google
- We may receive a confirmation token from Apple/Google indicating you have an active subscription
- The corresponding privacy policies of Apple/Google govern the payment process

---

## 12. Changes to This Policy

We may update this policy from time to time. The "Last Updated" date at the top reflects the most recent change. Material changes will be communicated via an in-app notice or release notes. Continued use of the App after changes constitutes acceptance.

---

## 13. Contact

Questions, concerns, or data requests:
**[YOUR EMAIL]**

---

## 14. Disclaimer (Not Legal Advice)

The App and its content (contract templates, glossaries, market scores, deal analyses) are provided for **educational and informational purposes only**. Nothing in the App constitutes legal, tax, accounting, or investment advice. Always consult a licensed real estate attorney, CPA, and/or financial advisor in your state before making investment or contractual decisions.
