High Priority SEO / Local SEO / CRO Fixes Package
Commit: c8dca2a

Placement instructions
----------------------
Copy each file in this ZIP into the repository root of fsilver79/vendotucasapr.

Replace these existing files:
- index.html
- privacy.html
- thank-you.html
- felix-foto.png

Add these new files at the repository root:
- robots.txt
- sitemap.xml
- felix-foto.webp

Files included
--------------
- index.html
- privacy.html
- thank-you.html
- robots.txt
- sitemap.xml
- felix-foto.webp
- felix-foto.png

Summary of changes implemented
------------------------------
1. Added robots.txt with a sitemap reference.
2. Added sitemap.xml listing the homepage and privacy page.
3. Added canonical tags to index.html, privacy.html, and thank-you.html.
4. Added JSON-LD structured data for Felix Silvestrini Real Estate as a RealEstateAgent / LocalBusiness serving Puerto Rico.
5. Connected all lead form labels to their corresponding fields using for/id.
6. Updated the form handler so failed webhook submissions show an inline error instead of redirecting to thank-you.html.
7. Added an inline form error message with role="alert".
8. Fixed invalid nested anchor markup in the form success message.
9. Added felix-foto.webp as a smaller hero image and updated the hero image to use a picture element with PNG fallback.
10. Optimized felix-foto.png as the fallback image.
11. Added width, height, decoding, fetchpriority, loading, and preload hints where appropriate.
12. Fixed the mobile buyers section by adding the missing compradores-grid ID that the existing mobile CSS selector expects.

Manual testing checklist
------------------------
- Confirm the homepage loads and the hero image appears correctly.
- Confirm /robots.txt and /sitemap.xml are reachable after deployment.
- Use a structured data validator to confirm the JSON-LD parses.
- Submit the lead form with a successful webhook response and confirm it redirects to /thank-you.html.
- Temporarily test a webhook failure and confirm the inline error appears instead of redirecting.
- Check the buyers section on a mobile viewport to confirm it becomes one column.
- Confirm privacy.html and thank-you.html still render normally.

Risks / review before merging
-----------------------------
- The form now requires a successful HTTP response before redirecting. If the Make webhook returns a non-2xx status even while processing the lead, users will see the error message.
- The WebP hero image is much smaller and should look visually the same at the displayed size, but the deployed page should be checked on mobile and desktop.
- sitemap.xml intentionally excludes thank-you.html because it is a conversion confirmation page, not a search landing page.
