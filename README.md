# auth-screens CDN mirror

Public mirror of the compiled Auth0 Advanced Customizations for Universal Login (ACUL) bundle produced by `apps/auth-screens` in the `infinite1-monorepo` repository.

> Do not edit these files by hand. They are generated artifacts. All changes must originate from the source repository.

## How it is served

Files in this repository are served publicly over HTTPS via [jsDelivr](https://www.jsdelivr.com/). Pinning by commit SHA ensures the bundle is content-addressable and compatible with Auth0's Subresource Integrity (SRI) requirement:

```
https://cdn.jsdelivr.net/gh/alejomo/test@<commit-sha>/index.js
https://cdn.jsdelivr.net/gh/alejomo/test@<commit-sha>/index.css
```

## Publish flow

1. In the source repo, build the bundle: `pnpm --filter auth-screens build`
2. Copy `apps/auth-screens/dist/*` into this repo's root
3. Commit and push
4. Use the resulting commit SHA in the Auth0 `prompts/*/screen/*/rendering` settings

This setup is intended for dev/testing only. Production should move to a properly governed CDN (e.g. Azure Blob Storage behind a corporate domain) with a CI pipeline.
