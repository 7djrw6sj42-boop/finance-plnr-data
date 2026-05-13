# Developer Finance Plnr — Master Launch Checklist
**Owner:** Donnie Gillespie
**Last updated:** May 10, 2026

---

## 📌 STATUS LEGEND

- ✅ DONE
- ⏳ IN PROGRESS
- ❌ NOT STARTED
- 🚫 BLOCKED (waiting on something)

---

# PART 1 — LAUNCH STEPS (in order)

## 🔴 Admin Tasks (only you can do these)

### Step 1 — Apple Developer Program enrollment
- [ ] Go to **developer.apple.com/programs/enroll**
- [ ] Sign in with Apple ID tied to your real identity
- [ ] Choose **Individual** (Organization needs DUNS number)
- [ ] Pay **$99/yr**
- [ ] Wait 24-48 hours for approval
- [ ] Confirmation email received

### Step 2 — Google Play Console account
- [ ] Go to **play.google.com/console**
- [ ] Pay **$25 one-time**
- [ ] Use same identity as Apple

### Step 3 — Privacy Policy hosted
- [x] ✅ DONE — Live at `https://7djrw6sj42-boop.github.io/finance-plnr-data/privacy.html`
- [x] ✅ Wired into Settings → Privacy Policy in app

### Step 4 — Support page / URL
- [ ] Create a simple HTML page with contact email
- [ ] Host on same GitHub Pages site
- [ ] URL ends up at `https://7djrw6sj42-boop.github.io/finance-plnr-data/support.html`
- [ ] Required field on App Store Connect listing

### Step 5 — Take screenshots
- [ ] Setup iOS simulator (Xcode → Simulator → iPhone 16 Pro Max) OR use real phone
- [ ] Required: at least 3 screenshots, max 10
- [ ] Resolution: 1290×2796 (iPhone 6.9" / 16 Pro Max)
- [ ] Suggested 7 screenshots:
  - [ ] **#1** Home dashboard (logo + stocks + rates visible)
  - [ ] **#2** Deal Analyzer with results filled in
  - [ ] **#3** Market Scorecard with verdict + insights
  - [ ] **#4** MAO Calculator with result
  - [ ] **#5** Driving for $$$ list with photos
  - [ ] **#6** Cash Buyers + Share modal
  - [ ] **#7** Helper bot conversation OR Contract Generator preview
- [ ] Optional: run through `app-mockup.com` for polished phone bezels
- [ ] Save raw + framed versions in `~/Desktop/DevFinancePlnr-Screenshots/`

---

## 🟡 Build Tasks (I can run for you)

### Step 6 — Set up EAS Build
- [ ] Install: `npm install -g eas-cli`
- [ ] Login: `eas login`
- [ ] Configure: `eas build:configure`
- [ ] Verify `eas.json` is created in project

### Step 7 — Build iOS app
- [ ] Run: `eas build --platform ios --profile production`
- [ ] Wait ~15-30 min for cloud build to complete
- [ ] Confirm `.ipa` artifact in EAS dashboard
- [ ] Free tier: ~30 builds/month

### Step 8 — Submit build to App Store Connect
- [ ] Run: `eas submit --platform ios`
- [ ] OR upload manually via **Transporter** app on Mac
- [ ] Build appears in App Store Connect after ~15 min processing

### Step 9 — Build + Submit Android
- [ ] Run: `eas build --platform android --profile production`
- [ ] Run: `eas submit --platform android`
- [ ] Submits to internal testing track first

---

## 🟢 Final Stretch (after build is uploaded)

### Step 10 — Fill App Store Connect form
- [ ] Pre-fill answers ready in [AppStoreFormFields.md](AppStoreFormFields.md)
- [ ] Sign in to **appstoreconnect.apple.com**
- [ ] Create new app (use values from form fields doc)
- [ ] Fill App Information tab — name, subtitle, bundle ID, primary language
- [ ] Fill Pricing — $0 free, all territories
- [ ] Fill Version 1.0 info — promotional text, description, keywords, what's new
- [ ] Upload icon (1024×1024 — already in project)
- [ ] Upload screenshots from Step 5
- [ ] Set categories — Finance / Business
- [ ] Run age-rating questionnaire (answer all "None" / "No" → results in 4+)
- [ ] Fill Privacy nutrition label (use pre-filled table)
- [ ] Set Privacy Policy URL: `https://7djrw6sj42-boop.github.io/finance-plnr-data/privacy.html`
- [ ] Set Support URL (from Step 4)
- [ ] Add review notes (use pre-written from form fields doc)

### Step 11 — TestFlight (recommended before public submit)
- [ ] In App Store Connect → TestFlight tab
- [ ] Add 5-10 internal testers (your email + friends/family)
- [ ] Send invite link
- [ ] Beta test for 1-2 weeks
- [ ] Collect feedback, fix bugs
- [ ] Iterate (rebuild via EAS, push update)

### Step 12 — Submit for App Review
- [ ] Final review of all metadata
- [ ] Click **Add for Review**
- [ ] Answer 3 final questions:
  - [ ] Export Compliance: encryption (HTTPS) → qualifies for exemption
  - [ ] Content Rights: third-party content → Yes (data sources)
  - [ ] Advertising Identifier (IDFA): No
- [ ] Submit
- [ ] **Wait 1-3 business days** for review

### Step 13 — Approval & Release
- [ ] Approval email received
- [ ] Click **Release** (or set automatic release on approval)
- [ ] Goes live globally within hours
- [ ] Confirm App Store listing is publicly searchable

### Step 14 — Google Play Production Release
- [ ] Move from Internal → Closed → Open testing
- [ ] Or skip straight to Production
- [ ] Google review usually <24 hours
- [ ] Confirm Play Store listing live

---

# PART 2 — PRE-BUILD FUNCTIONAL TEST (30-45 min)

Run through this BEFORE Step 7 (EAS Build). Better to catch bugs in dev.

## Tab Navigation
- [ ] All 6 bottom tabs load: Home, Tools, Pipeline, Files, More, Docs
- [ ] Each menu tab opens correctly
- [ ] Drilling into sub-screens works
- [ ] Back arrows return to menu screens
- [ ] Reference Docs accordion works (one open at a time)

## Home Screen
- [ ] Logo renders
- [ ] Stocks load real prices (pull to refresh works)
- [ ] Interest Rates load (FRED data)
- [ ] Quick Start cards navigate correctly
- [ ] What's New card no overflow

## Deal Analyzer + Form Persistence
- [ ] Type into fields → switch tab → return → fields preserved
- [ ] Calculate → results show
- [ ] **💾 Save** modal works → load saved deal restores
- [ ] **📤 Share** opens buyers picker
- [ ] **📄 PDF** generates and shares

## Rehab Budget
- [ ] Enter line items in 2-3 categories → calculate
- [ ] Variance card with colored alert pill
- [ ] Save / Share / PDF work

## MAO Calculator
- [ ] ARV / Rehab / Fee → calculate
- [ ] Result shows correct math
- [ ] Try Rule % = 80 (BRRRR mode)

## Market Scorecard
- [ ] City autocomplete works
- [ ] Lookup → live BLS + FBI data appears
- [ ] **Brooklyn, NY** → auto-redirects to "New York"
- [ ] Fake city → voids with error
- [ ] Manual sliders + total score work

## Contract Generators
- [ ] PSA: fill seller, buyer, ZIP (auto-fills city/state), price
- [ ] Generate → clean sectioned output
- [ ] **📋 Send to Title Co.** opens picker
- [ ] PDF export works
- [ ] Form persistence: leave mid-fill → return → still there
- [ ] Assignment Generator: same flow

## Pipeline
- [ ] Add Cash Buyer → call/text/email work
- [ ] Add Title Co → same
- [ ] Log a DfD lead with photo (camera permission prompt fires once)
- [ ] Filter chips work

## Files
- [ ] Photos gallery shows lead photos
- [ ] Tap photo → fullscreen modal
- [ ] Reports computes stats
- [ ] Calendar shows activity timeline

## More tab
- [ ] **Helper Bot** setup screen with Gemini/Claude picker
- [ ] **Settings** — each Clear button works
- [ ] **Partners** — all 14 cards render, links open browser
- [ ] **Privacy Policy** link opens hosted URL

---

# PART 3 — DEEPER TESTING (if you have time)

## Data Integrity / Cross-Screen
- [ ] Save deal → Reports stat updates?
- [ ] Save deal → Calendar event appears?
- [ ] BRRRR results auto-sync to Rehab Budget?
- [ ] Buyer with matching price → MATCH badge appears?
- [ ] Save 5+ deals → load each → all data restores?

## Network / API Resilience
- [ ] Airplane mode → Market Scorecard → graceful error?
- [ ] Bad RentCast key → clear error?
- [ ] Helper bot mid-conversation → kill WiFi → handles cleanly?
- [ ] FRED rates fail → Home screen still renders?

## iOS Quirks
- [ ] Rotate to landscape → nothing breaks?
- [ ] iOS Dark mode → readable?
- [ ] iOS system font scaled up → layout works?
- [ ] Long-press contract preview → can copy text?

## Multi-Device Sizes
- [ ] iPhone SE (smallest) → bottom tabs OK?
- [ ] iPhone 16 Pro Max → not too small?
- [ ] iPad → renders OK?

## Permissions
- [ ] Camera permission prompt fires once on first DfD use
- [ ] Deny camera → graceful handling?
- [ ] Re-enable in iOS Settings → next attempt works?

## URL / Linking
- [ ] Property Lookup → Zillow opens?
- [ ] DfD lead → Navigate → Apple Maps?
- [ ] Partners → all 14 links open valid URLs?
- [ ] Privacy policy in Settings opens browser?

## Long-Running State
- [ ] Fill form → wait 5 min → app killed → reopen → still there?
- [ ] Generate 5,000+ char contract → preview renders?
- [ ] 50+ DfD leads → list scrolls smoothly?
- [ ] Helper chat 50 messages → old history clipped properly?

## Boundary Inputs
- [ ] Purchase price = 0 → no div-by-zero
- [ ] ARV = $99,999,999 → display doesn't break
- [ ] Negative numbers → handled?
- [ ] Special chars in name (apostrophes, accents) → contract renders?
- [ ] Very long seller name → layout intact?

## PDF Export
- [ ] PDF on PSA → opens in Files / Mail / AirDrop?
- [ ] PDF for budget with 0 line items → renders?
- [ ] Special chars in seller name → renders cleanly?

## Settings / Wipes
- [ ] Wipe All App Data → returns to fresh install state?
- [ ] Clear Form Drafts → 5 form screens reset?
- [ ] Refresh state data → fetches latest from GitHub JSON?

---

# PART 4 — POST-LAUNCH TASKS

## Marketing (Week 1-4)
- [ ] Post in r/realestateinvesting with screenshots
- [ ] Post in r/wholesalerealestate
- [ ] Post in BiggerPockets forums
- [ ] Post in 3-5 FB wholesaler groups
- [ ] Submit to local REIA newsletter
- [ ] Make 1 walkthrough video → YouTube/IG/TikTok
- [ ] DM 20 active wholesalers on IG offering free use
- [ ] **Goal: 25 active users in 4 weeks**

## Affiliate Programs (apply for real revenue)
- [ ] Northwest Registered Agent — instant approval
- [ ] Stessa — investor-focused affiliate program
- [ ] Steadily — investor-friendly
- [ ] Kiavi / Lima One — broker programs
- [ ] BiggerPockets Pro
- [ ] PropStream
- [ ] DealMachine
- [ ] BatchLeads
- [ ] Replace `url` field in PartnersScreen.js with each approved affiliate link

## Analytics & Feedback
- [ ] Set up free email list (Buttondown, Substack, Mailchimp free tier)
- [ ] In-app feedback button → already wired (Send Feedback in Settings)
- [ ] App Store reviews — respond to all
- [ ] Track ratings / reviews

## v2 Backend Phase (when you have ~50+ users)
- [ ] See full plan in [V2_ROADMAP.md](V2_ROADMAP.md)
- [ ] Sign in with Apple/Google
- [ ] Cloud sync for saved data
- [ ] Server proxy for AI bot (replace BYOK)
- [ ] IAP for Pro tier ($9.99/mo)

---

# PART 5 — COSTS & TIMELINES

| Item | Cost | Time |
|---|---|---|
| Apple Developer | $99/yr | 24-48hr approval |
| Google Play | $25 once | Instant |
| App icon | $0 (you made it) | — |
| Privacy hosting | $0 (GitHub Pages) | Live now |
| EAS Build | $0 (free tier) | 30 min/build |
| App Review (Apple) | $0 | 1-3 business days |
| App Review (Google) | $0 | <24 hours |
| **TOTAL TO LAUNCH** | **~$125** | **~1-2 weeks** |

---

# PART 6 — WHAT'S DONE (as of May 10, 2026)

✅ App icon designed and placed in project
✅ Splash screen configured
✅ App metadata (bundle ID, version, theme)
✅ Privacy Policy hosted publicly
✅ Privacy Policy wired into Settings
✅ All v1 features built (10+ screens, 6 tabs)
✅ Deal Analyzer + MAO Calculator
✅ Market Scorecard with live Census/BLS/FBI data
✅ Property Lookup (Zillow/Redfin/County)
✅ Comp Pull (RentCast)
✅ Driving for $$$ with photo support
✅ Cash Buyers + Title Companies management
✅ Wholesale + Assignment Contract Generators (professional format)
✅ AI Rehab Helper Bot (Gemini + Claude)
✅ Save / Share / PDF / Send to Title Co. on every contract
✅ Auto-save form drafts across tab switches
✅ ZIP autofill on every relevant screen
✅ Reports + Calendar + Photos gallery
✅ Investor Tools & Partners page (14 affiliates)
✅ Settings with full data management
✅ Comprehensive in-app reference library + glossaries
✅ App Store listing copy drafted (4000 char description)
✅ App Store form fields pre-filled
✅ Privacy Policy template
✅ V2 Backend roadmap documented

---

*Print this page on Letter or A4. Tick boxes by hand. Ship it.* 🚀
