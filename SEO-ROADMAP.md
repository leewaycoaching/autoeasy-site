# Auto Easy Driving: SEO delivery roadmap

Website: https://autoeasydriving.co.uk/
Repository: leewaycoaching/autoeasy-site
Deployment: Cloudflare Pages
Purpose: increase qualified enquiries for automatic driving lessons in the genuinely served Poole and Bournemouth area, without sacrificing the current visual design.

## Current repository audit (19 Nov 2026)

- Static site: a single index.html plus images; no existing sitemap.xml or robots.txt in main at audit time.
- Homepage includes a descriptive title, description, canonical URL, Open Graph metadata, en-GB language attribute and two JSON-LD blocks.
- Strong visible content: Gillian's DVSA Grade A qualification, 30 years of instruction, nervous-learner positioning, prices, customer reviews, real pass photographs, service coverage and WhatsApp/call CTAs.
- Current architecture has one indexable content page. Additional topic-specific pages should be added only when they offer substantial unique, accurate information.
- This branch adds a robots.txt and a one-URL sitemap for the existing real page. Never list pages until they are published and return HTTP 200.

## Priority 0: verify baseline and indexing

- Connect and verify the domain property in Google Search Console (DNS verification). Review Page Indexing, URL Inspection and Performance reports.
- Submit https://autoeasydriving.co.uk/sitemap.xml once this branch is deployed.
- Verify that https://autoeasydriving.co.uk/ returns HTTP 200, that canonical matches, and that www and HTTP variations resolve or redirect consistently to the chosen HTTPS non-www URL.
- Check robots.txt and sitemap.xml publicly after deployment.
- Run PageSpeed Insights on mobile and desktop; record LCP, CLS, INP and image sizes. Avoid speculative "SEO scores".
- Confirm that Gillian's Google Business Profile links to this exact canonical site, has accurate phone, service area, business name and real reviews.

## Priority 1: site information architecture

Propose distinct, user-helpful pages, validated with Gillian's actual services and coverage:

1. /automatic-driving-lessons-poole/ (distinctive Poole-specific lessons, learner concerns and practical information)
2. /automatic-driving-lessons-bournemouth/ (genuinely Bournemouth-specific details, not rewritten location swaps)
3. /nervous-drivers/ (first-lesson process, previous negative experiences, confidence building)
4. /female-driving-instructor/ or /about-gillian/ (avoid overlapping thin pages; prioritise one strong profile page)
5. /prices/ (current transparent rate and terms)
6. /refresher-driving-lessons/ (only if actually offered, with specifics)

Requirements for every published page:
- One relevant, naturally worded H1, distinct title and helpful description.
- Self-referencing canonical URL, accurate content, crawlable text and navigational links.
- Visible contact details, appropriate conversion CTA and useful contextual internal links.
- Reusable accessible design and consistent typography with the homepage.
- Responsive layout and image dimensions/alt text where relevant.
- Add the URL to sitemap only after it is live.
- Avoid doorway pages, near-duplicate area pages, made-up testimonials, false service claims and keyword stuffing.

## Priority 2: local relevance & conversion

- Standardise the business name consistently with the real Google Business Profile and existing branding. Historic review quotations referencing AutoEazy should remain unchanged.
- Confirm service-area boundaries, whether Gillian offers pick-ups, and whether the quoted £80/90-minute rate and advertised hours are current.
- Add original instructor and local photos where consent exists and maintain descriptive alt text.
- Make booking, WhatsApp and phone links accessible and measurable; track enquiries with privacy-conscious analytics.
- Strengthen local relevance through genuine local information, not interchangeable neighbourhood keyword lists.

## Structured data guidance

- Review the existing JSON-LD for accurate name, URL, telephone, areaServed and services. Do not duplicate or invent rating or review data.
- Google limits FAQ rich results to select authoritative government/health sites: FAQ schema is not a shortcut to visible search enhancements.
- Validate structured data against the current visible page and Google's Rich Results Test.

## Collaboration/deployment

- Claude and ChatGPT should use separate branches and pull requests, not simultaneously edit main.
- Keep SEO work separate from design/font changes.
- Review Cloudflare Pages preview URLs and test before merging to main.
- Confirm Cloudflare Pages builds from main, then merge only after review; do not trigger production changes from this draft branch.

## Post-launch measurement

Record weekly: Search Console impressions, clicks, query/page positions, organic landing pages and real enquiries. Compare 28-day periods and avoid overinterpreting the first few weeks of a new domain.

## Evidence from 19 November 2026

### Live-site baseline (OpenSEO crawl, prior to publication)
- HTTP 200, indexable homepage, 2,477 words, one H1, 11 images and no missing alt text.
- Lighthouse mobile performance 84, desktop performance 97, SEO 92, accessibility 87.
- Mobile LCP in synthetic test ~3.61 sec. Main flagged opportunities: oversized hero image (original 1000×1333 JPEG ~266 KB), render-blocking Google Fonts, missing main landmark, review heading hierarchy, low-contrast labels and malformed robots.txt on production (HTML served at the path). Source fixes have been made in the draft except full image compression and font optimisations.

### Research-supported keyword priorities (approximate UK monthly volume)
- automatic driving lessons Bournemouth: ~210, KD 1 (tool estimate)
- automatic driving lessons Poole: ~90, KD 0
- female driving instructor Bournemouth: ~50, KD 0
- female driving instructor Poole: ~30, KD 0
- Other terms must be checked for useful demand before making thin pages. Search volume and difficulty estimates are not guaranteed traffic or Google rankings.

### Local-business profile discrepancy
- The existing Google Business Profile (CID 3573782846472705415) points to `www.bournemouthautomaticdrivinglessons.co.uk`, not the new domain.
- Public Google profile data currently shows 6 five-star reviews; prior homepage claimed 37. Real reviews may exist in other sources. Confirm before publishing any hard numbers. Self-serving `aggregateRating` structured data has been removed from the draft.
- Current Google profile hours differ from those printed on the website. Confirm real lesson hours with Gillian.
- Avoid inventing a precise business location; the unverified coordinates/address were removed from draft JSON-LD.

### Preview and go-live gate
- Preview has been crawled successfully: homepage plus three initial service pages returned 200, linked internally and canonicalised to the future production URLs. The `noindex` preview header is intentional on Cloudflare Pages.
- Additional female-instructor page is being added to this draft and should be preview-audited before publication.
- PR #1 is **draft**. No merge to main or change in production is permitted without an explicit approval.
- GitHub issue #2 contains Cloudflare / Search Console / Business Profile checklists.
- No recurring paid rank checks have been enabled: two local mobile rank trackers (Poole and Bournemouth) are set to manual.
