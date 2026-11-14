# Vorniqa Technologies landing page

Static HTML website for GitHub Pages. No paid domain, package installation, or build is required.

Website after publication: https://vorniqatechnologies-dotcom.github.io/vorniqatech/

## Publish now with GitHub Pages

1. Open https://github.com/vorniqatechnologies-dotcom/vorniqatech and make sure the repository is public for GitHub Free hosting.
2. Use **Add file → Upload files** to upload `index.html`, `favicon.svg`, `sitemap.xml`, and `robots.txt` to the repository root. Commit the files to your default branch (usually `main`). Replace an older `index.html` if present. You can also commit the provided `.nojekyll` file through your Git client; it bypasses Jekyll processing, but plain HTML does not require it.
3. Open **Settings → Pages**. Under **Build and deployment**, select **Deploy from a branch**, your default branch, and **/(root)**. Click **Save**. Leave **Custom domain** empty.
4. Wait for the Pages deployment to finish in **Actions**. Open the website URL above and confirm that it loads. Enable **Enforce HTTPS** if it is not already enabled.
5. Check that https://vorniqatechnologies-dotcom.github.io/vorniqatech/sitemap.xml loads as XML and that the page source contains the canonical URL and Google verification tag.

If this repository already has a deployment workflow, use one publishing method consistently. These instructions use GitHub's branch publishing; no custom workflow is supplied or required.

If the account or repository name changes, update the absolute URLs in `index.html`, `sitemap.xml`, and `robots.txt` together.

GitHub Pages usage limits: https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits
Pages has restrictions on sites primarily facilitating commercial transactions or providing commercial SaaS. This repository publishes only the informational landing page; do not use Pages to host the accounting application's backend or payment processing.

## Submit to Google after the site is live

1. Open https://search.google.com/search-console/ using the Google account that owns the existing verification token, or use your own account and replace the token as described below.
2. Add a **URL prefix** property with exactly `https://vorniqatechnologies-dotcom.github.io/vorniqatech/`. Use URL prefix because you do not control DNS for `github.io`.
3. Choose **HTML tag** verification. The existing `google-site-verification` tag is preserved in `index.html`. If Search Console gives you a different token, replace its `content` value, commit the change, wait for deployment, and click **Verify**. Keep the tag after successful verification.
4. In **Sitemaps**, submit `https://vorniqatechnologies-dotcom.github.io/vorniqatech/sitemap.xml`.
5. In **URL inspection**, inspect the homepage URL, run **Test live URL**, and choose **Request indexing** if the live test succeeds. Check **Page indexing** for Google's reported reason if the page remains excluded.

The sitemap contains just the homepage. Sections such as `#about`, `#solutions`, and `#contact` belong to the same document and should not be listed as separate pages. No fabricated modification dates are included.

Google reads robots rules only from `https://vorniqatechnologies-dotcom.github.io/robots.txt`, not from `/vorniqatech/robots.txt`. The supplied `robots.txt` is ready to copy to the root of a separate `vorniqatechnologies-dotcom.github.io` repository if you manage that root site. Its sitemap line points to this project. A missing root robots file does not block crawling. If a root robots file already exists, check that it allows `/vorniqatech/` and merge the sitemap line into it. Submit the sitemap directly through Search Console regardless.

Google says crawling can take days to weeks and does not guarantee indexing or ranking. No HTML change can guarantee immediate visibility, first position, or results for every spelling. The page includes the correct brand, a brief visible reference to the requested “Vorniqua” spelling, and relevant accounting and audit preparation terms. Google ignores the `keywords` meta tag for ranking; useful visible content and accurate business information matter.

References:

- https://developers.google.com/search/docs/crawling-indexing/ask-google-to-recrawl
- https://developers.google.com/search/docs/crawling-indexing/robots/intro
- https://developers.google.com/search/docs/crawling-indexing/special-tags

## Google Business Profile

Google Business Profile and Google Search indexing are separate processes. If eligible, add or claim your business at https://business.google.com/ and set the website to the Pages URL above. Complete Google's verification and use the real business name, category, phone, address or service area, and opening hours consistently.

Eligibility generally requires a location customers can visit or a business that travels to customers. Online-only businesses are not eligible. A free GitHub URL does not establish business eligibility, and adding schema does not create or verify a Business Profile. No street address, phone number, reviews, opening hours, or local business claims have been invented in this page.

Eligibility guidance: https://support.google.com/business/answer/3038177

## Existing contact forms need configuration

The original page still has `YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL` as its form endpoint. It currently displays success messages without a working destination; those messages do not prove a request was delivered. Configure and verify a real form endpoint before relying on demo requests. The visible email address now has a working `mailto:` link so visitors can email directly.

Tailwind CSS, icons, and fonts use external CDNs, as in the original page. Page text and structured information are present directly in the HTML and do not require JavaScript to be discovered.
