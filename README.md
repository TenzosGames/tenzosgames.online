# TenzosGames website

Static English studio website for `tenzosgames.online`. The publishing account must be **TerencezosGames**. The site has no build step or external code dependency.

## Files to publish

Publish the contents of this folder at the root of a dedicated public GitHub repository: `index.html`, `support.html`, `privacy-policy.html`, `styles.css`, `favicon.svg`, `CNAME`, and `.nojekyll`. Do not publish files from the parent workspace or another studio's site.

## GitHub Pages

In the repository's **Settings → Pages**, choose **Deploy from a branch**, branch `main`, folder `/(root)`. Set the custom domain to `tenzosgames.online`; after DNS and certificate provisioning, turn on **Enforce HTTPS**. The `CNAME` file contains the same apex domain.

## Alibaba Cloud DNS

For the apex (`@`), add these four `A` records:

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

For `www`, add a `CNAME` pointing to `TerencezosGames.github.io`. Remove conflicting default/parking records for `@` and `www`. GitHub recommends configuring both apex and `www` so it can redirect the alternate hostname. Do not use a wildcard record. These values were checked against [GitHub's custom-domain documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) on 2026-10-09.

## Final URL checks

- `https://tenzosgames.online/`
- `https://tenzosgames.online/support.html`
- `https://tenzosgames.online/privacy-policy.html`
- `https://tenzosgames.online/privacy-policy.html#california`
- `https://www.tenzosgames.online/` should redirect to the configured apex.

Only use the final HTTPS URLs in store listings after they load reliably.

## Before linking a specific game

Confirm that the game's binary actually contains the eight named advertising partners, and that the exact SDK versions and settings match the policy. Configure and test any required EEA/UK/Swiss consent flow before applicable SDK processing; transmit consent choices to each mediated partner, including partners needing separate configuration. Match iOS App Tracking Transparency behavior, App Store Connect privacy answers, Android/Data safety answers, age settings, and applicable US state sale/sharing opt-out handling. Verify that rights and opt-out email requests reach the support mailbox. Update this policy if a game adds other data processing, features, SDKs, or precise location.
