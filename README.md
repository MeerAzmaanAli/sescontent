# SES content repository

`site.json` is the single source of truth for reusable company content. Move this folder into a separate public repository when ready, then serve the raw JSON from GitHub Pages, a CDN, or a small API.

The website first requests `window.SES_CONTENT_API_URL` when configured, then falls back to `SES_content/site.json`. This keeps every page usable during API outages and local development.

Example remote endpoint:

```html
<script>window.SES_CONTENT_API_URL = 'https://meerazmaanali.github.io/sesSES_content/site.json';</script>
```

## Project photos

Each item in `site.json` > `projects` supports this structure:

```json
{
  "slug": "warehouse-fire-suppression-retrofit",
  "status": "Delivered",
  "scope": ["Full sprinkler and detection retrofit across a multi-bay logistics warehouse."],
  "gallery": [
    { "src": "https://your-image-host.example/project-01.jpg", "alt": "Installed sprinkler network" }
  ]
}
```

Use publicly accessible image URLs in `gallery`. After committing and publishing the update, the project detail page will show the photos automatically.