# App Store Connect — Form Fields Cheat Sheet
**Pre-filled values for every field. Copy/paste directly into App Store Connect.**

> 📌 Items marked **[YOU FILL]** require your personal info or decisions.
> Items marked **[NEEDS HOSTING]** require a public URL you set up first.

---

## 🆕 Step 1 — Create New App

When you click "+" → New App in App Store Connect:

| Field | Value |
|---|---|
| **Platforms** | iOS (check the box; add macOS later if you want) |
| **Name** | `Developer Finance Plnr` |
| **Primary Language** | English (U.S.) |
| **Bundle ID** | `com.[YOU FILL].devfinanceplnr` (must match what's in `app.json` — register a new one in Apple Developer → Certificates, Identifiers & Profiles → Identifiers) |
| **SKU** | `DEVFINPLNR001` (any unique string — used for your accounting only, never visible to users) |
| **User Access** | Full Access |

---

## 📋 Step 2 — App Information Tab

### Localizable Information (English U.S.)

| Field | Value |
|---|---|
| **Name** | `Developer Finance Plnr` |
| **Subtitle** *(30 char max)* | `Wholesale & BRRRR Toolkit` |
| **Privacy Policy URL** | **[NEEDS HOSTING]** Your hosted privacy.html URL (e.g., `https://[USER].github.io/finance-plnr-data/privacy.html`) |
| **Privacy Choices URL** *(optional)* | Leave blank |

### General Information

| Field | Value |
|---|---|
| **Bundle ID** | (auto-filled from Step 1) |
| **SKU** | (auto-filled from Step 1) |
| **Primary Category** | `Finance` |
| **Secondary Category** | `Business` |
| **Content Rights** | "Does Your App Contain, Show, or Access Third-Party Content?" → **Yes** (RentCast, Anthropic, Census/BLS/FBI/FRED data — all licensed for use) |
| **Age Rating** | Run questionnaire (instructions below) |

### Age Rating Questionnaire

Click "Edit" next to Age Rating. Answer:

- **Cartoon or Fantasy Violence** → None
- **Realistic Violence** → None
- **Sexual Content or Nudity** → None
- **Profanity or Crude Humor** → None
- **Alcohol, Tobacco, or Drug Use** → None
- **Mature/Suggestive Themes** → None
- **Horror/Fear** → None
- **Medical/Treatment Information** → None
- **Gambling and Contests** → None
- **Unrestricted Web Access** → No
- **Social Networking** → No
- **Made for Kids** → No

**Result: 4+** (the most permissive rating)

---

## 💲 Step 3 — Pricing and Availability

| Field | Value |
|---|---|
| **Price Schedule** | `USD 0 (Free)` for all territories |
| **Availability** | All 175 countries/regions (default) — uncheck any you don't want |
| **Volume Purchase Program** | Not enrolled (default) |
| **Pre-Orders** | Not available (default) |

---

## 📱 Step 4 — Version Information (1.0)

This is the screen-by-screen content most users will see.

### Promotional Text *(170 char max — editable any time, no review)*

```
Run the numbers, source contracts, and pick markets in minutes. Built for real estate wholesalers and BRRRR investors. Free, no signup, your data stays on your phone.
```

### Description *(4000 char max)*

```
The complete toolkit for real estate wholesalers and BRRRR investors.

Stop juggling 6 different apps and a Google Sheet. Developer Finance Plnr puts deal analysis, market data, contracts, and rehab budgeting in one place — designed by investors, for investors.

WHAT'S INSIDE

🏠 Deal Analyzer (BRRRR)
Run the numbers on any deal in 30 seconds. Calculate cash-on-cash return, cap rate, monthly cash flow, equity gained, and refinance projections. Built around the 70% rule.

⚡ MAO Calculator
Quick maximum allowable offer math. Input ARV + rehab + your fee, get the most you should pay. Auto-flags negative-margin deals.

🔨 Rehab Budget Tool
10 detailed line-item categories — Demo, Exterior, Systems, Kitchen, Baths, Flooring, Walls/Paint, Doors, Lighting, Permits. Auto-compares your budget to your Deal Analyzer projection and flags variance over 15%. Cost-per-sqft + contingency built in.

📊 Market Scorecard with Live Data
Type a city + state. We pull real-time data from US Census, Bureau of Labor Statistics, and FBI to score the market: population growth, unemployment, property tax, income tax, violent crime, education rank, and landlord-friendliness.

📍 Property Lookup
Enter any US address. ZIP auto-fills city + state. One tap to open the property in Zillow, Redfin, or county records. Compare value estimates side by side.

🎯 Comp Pulls (RentCast)
Pull AVM, rent estimate, full property record, and 5 comparable sales for any address. Free 50 calls/month with your own RentCast key.

🚗 Driving for Dollars
Log distressed properties on the road with photo + notes in under 30 seconds. Auto-link to Zillow research and Apple Maps navigation. Track lead → researched → contacted → closed.

👥 Cash Buyers List
Track investors ready to take down deals. Call, text, or email any buyer in 1 tap. Auto-stamps last contact date so you can spot stale relationships.

📤 Share Deal With Buyer
After analyzing a deal, instantly share the summary with matching buyers via text, email, or any app. Auto-detects which buyers fit by price range and ZIP.

📝 Wholesale + Assignment Contracts
Generate Purchase & Sale Agreements with assignment clauses, plus full Assignment of Contract documents. 23+ standard sections including liquidated damages, specific performance, lis pendens, ESIGN-compliant signatures. Share via Messages, email, or PDF.

🤖 Rehab Helper Bot (optional)
Ask anything about wholesale deals, BRRRR strategy, permits, contracts, or contractor management. Powered by Claude AI with your own API key.

📚 Reference Library
Wholesaler Master Guide (10-step legal workflow), BRRRR Strategy Guide, Scope of Work Template, Contractor & Sub Playbook (red flags + costly mistakes), Seller Scripts, Rehab Glossary (40+ construction terms), Real Estate Glossary (70+ deal terms).

📁 Property Files
Photo gallery from your DfD leads, performance reports across saved deals (avg margin, cash flow, ROI), activity timeline grouped by day.

💰 Live Markets
Daily updates on housing-related stocks (ITB, XHB, VNQ, DHI, LEN, PHM, HD, LOW, BLDR) and interest rates (Fed Funds, 10/15/30-yr Treasury, 30-yr & 15-yr mortgage) — pulled live from FRED and Yahoo Finance.

💾 Save & Export
Save unlimited deals and rehab budgets to your phone. Export any deal, budget, or contract as a PDF.

PRIVACY
Your data stays on your phone. We don't have a server. We don't collect anything. No accounts, no ads, no tracking.

NOT LEGAL ADVICE
Templates are educational starting points — always have a licensed real estate attorney in your state review before signing real contracts.

Free. No signup required.
```

### Keywords *(100 char total, comma-separated, no spaces after commas)*

```
wholesale,BRRRR,real estate,deal analyzer,investor,rehab,property,landlord,flip,contract,investing,REI
```

### What's New in This Version *(release notes for v1.0)*

```
Initial release — built for wholesalers and BRRRR investors who want one app instead of seven.
Try it free, your data stays on your phone.
```

### Support URL *(required)*

**[YOU FILL]** Suggested options:
- `https://[USER].github.io/finance-plnr-data/` (use a simple "Get Help" page)
- A `mailto:` won't work — Apple requires HTTPS
- Easiest: create a one-page GitHub Pages site with `support.html` linking to your email

### Marketing URL *(optional)*

Leave blank for v1, or use the same support URL.

### Copyright

```
© 2026 [YOU FILL — Your Name or Company LLC]
```

### Trade Representative Contact (Korea only)

Leave blank — only required if shipping to Korea.

### Routing App Coverage File

Leave blank — only relevant for navigation/maps apps.

---

## 🖼️ Step 5 — Screenshots & App Preview

### Required: iPhone 6.9" Display *(iPhone 16 Pro Max — 1320×2868 px)*

**Need 3-10 screenshots, in this order:**

1. **Home Dashboard** — caption: *"Live mortgage rates and real estate stocks"*
2. **Deal Analyzer Results** — caption: *"Run the numbers in 30 seconds"*
3. **Market Scorecard** — caption: *"Score any US market with live data"*
4. **Wholesale Contract Generator** — caption: *"Attorney-grade contracts in seconds"*
5. **Driving for $$$** — caption: *"Log distressed properties on the go"*
6. **Cash Buyers + Share** — caption: *"One-tap deal blasts to matching buyers"*
7. **Rehab Helper Bot** — caption: *"Ask any wholesale or rehab question"*

**Tip:** Take raw screenshots, then run through `app-mockup.com` for polished bezel framing.

### iPhone 6.5" Display *(optional, 1242×2688)*
Apple auto-scales from 6.9" if you skip this.

### iPad Pro Displays
Skip unless you specifically want iPad listing.

### App Preview Video
Skip for v1 — adds production time without adding much conversion.

---

## 📊 Step 6 — App Privacy (Nutrition Label)

This is the most-changed section in App Store Connect. Click "Get Started" or "Edit" under "App Privacy."

**First question: "Do you or your third-party partners collect data from this app?"**

**Answer: Yes** *(because users opt into Anthropic + RentCast, even though we don't see it)*

### Data Types Collected

For each data type below, you'll see categories like "Used for Tracking", "Linked to You", "Not Linked to You". For our app:

| Data Type | Collected? | Linked to User? | Used for Tracking? | Why we use it |
|---|---|---|---|---|
| **Contact Info → Name** | No | — | — | — |
| **Contact Info → Email** | No | — | — | — |
| **Contact Info → Phone** | No | — | — | — |
| **Contact Info → Other** | No | — | — | — |
| **Health & Fitness** | No | — | — | — |
| **Financial Info → Payment** | No | — | — | — |
| **Financial Info → Other (Deal data)** | **Yes — but stored on device only** | Not Linked | No | App functionality (saved deals, budgets, contracts). Stays on device. |
| **Location → Precise** | No | — | — | — |
| **Location → Coarse** | No | — | — | — |
| **Sensitive Info** | No | — | — | — |
| **Contacts** | No | — | — | — |
| **User Content → Photos** | **Yes — on device only** | Not Linked | No | Photos for Driving for Dollars leads stay on device. |
| **User Content → Audio Data** | No | — | — | — |
| **User Content → Other (Address)** | **Yes — sent to selected APIs** | Not Linked | No | Property addresses sent to RentCast/Census/Zippopotam.us per user request. |
| **Browsing History** | No | — | — | — |
| **Search History** | No | — | — | — |
| **Identifiers → User ID** | No | — | — | — |
| **Identifiers → Device ID** | No | — | — | — |
| **Purchases → Purchase History** | No | — | — | — |
| **Usage Data → Product Interaction** | No | — | — | — |
| **Usage Data → Advertising Data** | No | — | — | — |
| **Diagnostics → Crash Data** | No | — | — | — |
| **Diagnostics → Performance Data** | No | — | — | — |
| **Other → Other Data Types** | No | — | — | — |

> 💡 **Honest path**: Apple's "data not collected" requires the app to literally not transmit the data. Since users opt-in to send addresses to RentCast and messages to Anthropic, you should disclose those even though they're optional. Apple cares about transmission, not storage.

---

## 🔒 Step 7 — App Review Information

### Sign-In Required?

**No** — app works without any account.

### Demo Account

Skip — no login.

### Notes for App Review *(important — this is what reviewers read)*

```
This app is a real estate investing toolkit for wholesalers and BRRRR investors. All features work offline-first; data is stored locally on the device only.

Features that require optional setup:
- Rehab Helper Bot: Users provide their own Anthropic API key (free $5 starter credit at console.anthropic.com).
- Comp Pull: Users provide their own RentCast API key (free 50 lookups/month at rentcast.io).

These are clearly marked as optional setup screens. The vast majority of features work without any external service or API key.

Live data sources (no key required):
- US Census Bureau (city population)
- Bureau of Labor Statistics (state unemployment)
- FBI Crime Data (state violent crime)
- FRED (Federal Reserve mortgage rates and Treasury yields)
- Yahoo Finance (housing-related stock prices)
- Zippopotam.us (ZIP to city/state lookup)

Contract templates included are educational starting points — disclosed in the app and the description as not legal advice.
```

### Contact Information for Reviewer

| Field | Value |
|---|---|
| **First Name** | [YOU FILL] |
| **Last Name** | [YOU FILL] |
| **Phone Number** | [YOU FILL] |
| **Email** | [YOU FILL] (use a real, monitored email) |

### Attachment

If a reviewer rejects asking for clarification, you can re-upload with a screen recording. Skip on initial submission.

---

## 🚀 Step 8 — Submit for Review

1. Make sure your build is uploaded and selected (via EAS or Transporter)
2. Click **Add for Review** at top right
3. Answer 3 final questions:
   - **Export Compliance**: "Does your app use encryption?" → Yes (HTTPS counts), but "qualifies for export compliance exemption" since you're using standard iOS HTTPS only.
   - **Content Rights**: "Does your app contain, display, or access third-party content?" → Yes (data sources)
   - **Advertising Identifier**: "Does your app use the Advertising Identifier (IDFA)?" → No
4. Submit

**Wait time: 1-3 business days typical. Approval emails arrive at your Apple Developer email.**

---

## 🤖 Google Play Console — Same Fields, Different Layout

When you do Play Store afterward, most of the same content reuses:

| Play Console Field | Reuse from above |
|---|---|
| App name | "Developer Finance Plnr" |
| Short description (80 char) | "Wholesale & BRRRR toolkit. Deal analysis, contracts, market data, lead pipeline." |
| Full description | Same as App Store description above |
| Category | Finance |
| Content rating | Everyone (similar to 4+) |
| Privacy policy URL | Same hosted URL |
| Screenshots | Reuse iPhone shots — Play accepts most sizes |
| Data safety form | Match the App Privacy answers above |

---

## 📝 Pre-Launch Checklist

Print this. Tick them off:

- [ ] Apple Developer account active ($99/yr)
- [ ] Bundle ID registered in Apple Developer portal
- [ ] Privacy policy hosted at public URL
- [ ] Support URL hosted (or mailto-only landing page)
- [ ] App icon 1024x1024 PNG ready
- [ ] 3-7 iPhone screenshots ready
- [ ] EAS build completed and uploaded
- [ ] All form fields filled per this doc
- [ ] App Privacy nutrition label completed
- [ ] App Review notes filled in
- [ ] Submitted for review
- [ ] (Optional) Internal testers added to TestFlight
- [ ] After approval: hit "Release"

---

*Last updated: 2026-05-07*
