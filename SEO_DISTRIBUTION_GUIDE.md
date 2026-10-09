# CS Brewed — Web Visibility & Off-Page SEO Playbook

This playbook provides actionable, step-by-step guidance for Phase 4 of the CS Brewed visibility strategy: search console verification, App Store optimization loops, directory submissions, and community distribution.

---

## 1. Search Engine Console Verification

### A. Google Search Console (GSC)
1. Navigate to [Google Search Console](https://search.google.com/search-console).
2. Choose **Domain** property: enter `csbrewed.com`.
3. Verify via **DNS TXT record** in your domain registrar (Namecheap):
   - Type: `TXT Record`
   - Host: `@`
   - Value: `google-site-verification=...`
   *(Alternative: HTML tag in `<head>` of `index.html`)*
4. Once verified, go to **Sitemaps** &rarr; Submit: `https://csbrewed.com/sitemap.xml`.
5. Run the **URL Inspection Tool** on `https://csbrewed.com/` and click **Request Indexing**.
6. Verify rich snippet recognition using the [Google Rich Results Test](https://search.google.com/test/rich-results) — it should detect `WebSite`, `Organization`, `ItemList` (SoftwareApplication), and `FAQPage`.

### B. Bing Webmaster Tools & IndexNow
1. Navigate to [Bing Webmaster Tools](https://www.bing.com/webmasters).
2. Click **Import from Google Search Console** (instant verification without adding new DNS records).
3. Submit `https://csbrewed.com/sitemap.xml`.
4. *Impact*: Bing indexes feed DuckDuckGo, Yahoo Search, and Microsoft Copilot.

---

## 2. App Store Connect (ASO <-> Web Synergies)

High-ranking web domains pass domain authority and organic referrals to the App Store, and App Store listings pass authoritative backlinks to your website.

For each app in **App Store Connect**:
1. **Teeth — Dental Journal**:
   - **Marketing URL**: `https://teeth.csbrewed.com/` (or `https://csbrewed.com/#teeth`)
   - **Support URL**: `https://csbrewed.com/#about` or `mailto:serjios19@gmail.com`
   - **Privacy Policy URL**: `https://teeth.csbrewed.com/privacy` or `https://csbrewed.com/#philosophy`
2. **The Surf Hero**:
   - **Marketing URL**: `https://the-surf-hero.csbrewed.com/`
   - **Support URL**: `https://csbrewed.com/#about`
3. **Perespiv**:
   - **Marketing URL**: `https://csbrewed.com/#perespiv`
   - **Support URL**: `https://csbrewed.com/#about`

---

## 3. Directory Submissions & Backlink Catalogs

High-quality backlinks from developer and software catalogues dramatically boost domain ranking for Apple software searches.

### A. AlternativeTo (High Conversion & High SEO Authority)
- **The Surf Hero**:
  - Submit as an alternative to: *Velja*, *Browserosaurus*, *OpenIn*, *Bumpr*.
  - Highlights: Menu bar native utility, lightweight, custom domain exception rules, zero tracking.
- **Teeth — Dental Journal**:
  - Submit as an alternative to: *Dental Note*, *Dental Tracker*, generic health notes.
  - Highlights: 100% on-device privacy, standard dental tooth numbering chart, visit history.

### B. macOS & iOS Software Catalogs
- [MacUpdate](https://www.macupdate.com/) — List The Surf Hero.
- [Softpedia Mac](https://mac.softpedia.com/) — Submit The Surf Hero.
- [AppAdvice](https://appadvice.com/) — Submit Teeth and Perespiv for review.
- [IndieAppList](https://indieapplist.com/) — Directory for independent Apple developers.

### C. Indie Hacker & Startup Directories
- **Product Hunt**: Schedule launches for *The Surf Hero* and *Teeth*.
- **BetaList**: Feature new versions or upcoming apps.
- **Indie Hackers**: Create a studio product page for *CS Brewed*.
- **Hacker News**: Post a *"Show HN: The Surf Hero – lightweight macOS default browser changer"* and *"Show HN: Teeth – privacy-first dental timeline for iPhone"*.

---

## 4. Community Showcase & Content Strategy

### Reddit Communities
Share helpful, non-spammy dev stories focusing on solving specific user frustrations:
- `r/macapps`: Share The Surf Hero's focus on menu bar speed and custom rules.
- `r/iOSProgramming` & `r/SwiftUI`: Post technical write-ups (e.g. building smooth screenshot sliders or offline-first SwiftData storage).
- `r/SideProject` & `r/indiebiz`: Studio launch story.

### GitHub Presence
- Tag repositories with relevant topics: `swift`, `swiftui`, `macos-utility`, `ios-app`, `privacy-first`, `indie-developer`.
- Include `https://csbrewed.com` in your GitHub profile bio (`schornon`) and profile README.

---

## 5. Answer Engine Optimization (AEO / GEO)

AI search engines (Perplexity, ChatGPT Search, Apple Intelligence) consume plain-text structured knowledge.
- Keep `llms.txt` up to date with new apps and releases.
- Maintain accurate Schema.org JSON-LD structured data on all pages.
- Ensure FAQ questions reflect natural phrasing people speak or type into AI prompts.
