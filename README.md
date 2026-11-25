# Take&Find website

Static public website for Take&Find. It contains:

- `index.html` — product introduction and SEO landing page
- `support.html` — App Store support URL and help content
- `privacy.html` — App Store privacy-policy URL
- `sitemap.xml`, `robots.txt`, structured data, Open Graph and Twitter metadata
- `404.html` for static hosting
- `_headers` for Cloudflare Pages security and cache headers

Support and privacy contact:

```text
13911100061@163.com
```

Current public URL:

```text
https://wbs21.github.io/takeandfind/
```

Indexing timing: **wait until Take&Find is officially available on the App Store
before submitting the sitemap or requesting indexing.** `sitemap.xml`,
`robots.txt`, and the SEO metadata remain ready for that later submission.

## Preview locally

From this directory:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080/`.

## Deploy

The site has no build step. Deploy the contents of this directory as the web root.

For GitHub Pages:

1. Publish the contents of this directory at the root of the
   `wbs21/takeandfind` GitHub Pages site.
2. Keep the project path `/takeandfind/`.
3. Do not add a repository-root `CNAME` while using the GitHub Pages hostname.

The canonical URL is `https://wbs21.github.io/takeandfind/`. If a custom domain
is introduced later, update the canonical, Open Graph, structured data, sitemap,
robots, and manifest URLs together.

## Google indexing

Google no longer accepts anonymous sitemap pings. Submission requires a live
public URL and access to Google Search Console:

1. Confirm the deployed site is available over HTTPS.
2. Add the URL-prefix property
   `https://wbs21.github.io/takeandfind/` in Search Console.
3. Verify ownership with the HTML verification file provided by Search Console.
   DNS verification is not available for the `github.io` hostname.
4. Place the verification file at the site root and redeploy before verifying.
5. Submit `https://wbs21.github.io/takeandfind/sitemap.xml`.
6. Use URL Inspection and **Request indexing** for:
   - `https://wbs21.github.io/takeandfind/`
   - `https://wbs21.github.io/takeandfind/support.html`
   - `https://wbs21.github.io/takeandfind/privacy.html`
