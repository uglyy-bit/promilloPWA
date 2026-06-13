# promillo

A small PWA that estimates your blood alcohol concentration (Promille), lets you
log drinks during a session and shows when you'll be sober again.

**Live app:** https://uglyy-bit.github.io/promilloPWA/

Just open the link in any browser. On a phone you can also tap "Add to Home
Screen" to install it like a native app.

## How it's hosted

This repo contains the built Flutter web output in the [`web/`](web/) folder.
On every push to `main`, the GitHub Actions workflow in
[`.github/workflows/deploy.yml`](.github/workflows/deploy.yml) publishes that
folder to GitHub Pages.

## Updating the app

Rebuild in your Flutter project and copy the fresh output into `web/`:

```bash
flutter build web --base-href /promilloPWA/
```

Then copy the contents of your project's `build/web/` into this repo's `web/`
folder, commit and push. The `--base-href /promilloPWA/` flag is important so the
app works under the `/promilloPWA/` subpath on GitHub Pages.
