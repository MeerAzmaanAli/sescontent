# SES content repository

`site.json` is the single source of truth for reusable company content. Move this folder into a separate public repository when ready, then serve the raw JSON from GitHub Pages, a CDN, or a small API.

The website first requests `window.SES_CONTENT_API_URL` when configured, then falls back to `content/site.json`. This keeps every page usable during API outages and local development.

Example remote endpoint:

```html
<script>window.SES_CONTENT_API_URL = 'https://content.example.com/site.json';</script>
```
