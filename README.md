# OwnStats Test Site

A minimal two-page static site for testing an OwnStats analytics tracking script.

## Structure

```
/
├── index.html   # Home page with a trackable click button
├── about.html   # Second page for multi-page-view testing
├── styles.css   # Shared styles
└── README.md
```

## Adding the OwnStats script

Each HTML file contains this placeholder comment inside `<head>`:

```html
<!-- OwnStats tracking script goes here -->
```

Replace that comment with the `<script>` tag provided by your OwnStats instance.

## Deploying to GitHub Pages

1. Push this repository to GitHub (ensure the files are in the root of the repo or a `/docs` folder).
2. Go to **Settings > Pages** in your GitHub repository.
3. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)` (or `/docs` if you placed the files there)
4. Click **Save**.
5. GitHub will publish the site at `https://<your-username>.github.io/<repo-name>/`.

> Changes pushed to `main` are automatically redeployed within a minute or two.

## Testing checklist

- [ ] Navigate Home -> About -> Home to generate multiple page views
- [ ] Click the "Click me to test tracking" button on the Home page
- [ ] Confirm both events appear in your OwnStats dashboard
