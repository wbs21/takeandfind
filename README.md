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

## Preview locally

From this directory:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080/`.

## Deploy

The site has no build step. Deploy the contents of this directory as the web root.

For Cloudflare Pages:

1. Connect the repository.
2. Set the project root to `website`.
3. Leave the build command empty.
4. Set the output directory to `.`.
5. Add `takeandfind.app` as a custom domain after registering it.

For GitHub Pages:

1. Publish this directory with Pages.
2. After registering the production domain, add a `CNAME` file containing only
   that hostname.
3. Configure the DNS records requested by GitHub.

The intended canonical URL is `https://takeandfind.app/`. Replace it everywhere
before deployment if the final production domain is different. Do not add a
custom-domain `CNAME` before the domain is actually owned and configured.

## Google indexing

Google no longer accepts anonymous sitemap pings. Submission requires a live
public URL and access to Google Search Console:

1. Deploy the site over HTTPS.
2. Add a Domain property or URL-prefix property in Search Console.
3. Verify ownership through DNS or the supplied HTML verification file/tag.
4. Submit `https://takeandfind.app/sitemap.xml`.
5. Use URL Inspection and **Request indexing** for:
   - `https://takeandfind.app/`
   - `https://takeandfind.app/support.html`
   - `https://takeandfind.app/privacy.html`

Do not submit until the canonical hostname, DNS, and HTTPS certificate are live.
