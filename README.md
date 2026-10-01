# ZEBRACODE domain redirect

This small GitHub Pages site sends visitors from `zebracode.tv` to the existing band website at `https://www.zebracode.tv/`.

The band website remains hosted on Cloudflare Pages. The domain registration and DNS remain managed by Wix. Only the apex A records point to GitHub Pages; the `www` CNAME remains `zebracode-band.pages.dev`.

The redirect happens in the browser using `location.replace`, retaining the path, query string, and fragment. Without JavaScript, a meta refresh and link lead to the homepage. This is not an HTTP 301 redirect.

Publish the `main` branch root with GitHub Pages, set the custom domain to `zebracode.tv`, and enable HTTPS after GitHub issues the certificate. Keep the GitHub domain-verification TXT record at Wix.

If this redirect is retired, remove or replace the apex DNS records before disabling the Pages site or deleting this repository.
