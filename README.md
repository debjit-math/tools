# Tools — GitHub Pages Toolkit

A responsive, searchable directory of interactive HTML tools. The homepage reads `tools.json`; each tool lives in `tools/<slug>/index.html`.

## Publish on GitHub Pages
1. Create a GitHub repository (for example, `tools`).
2. Upload the contents of this folder to the repository root, so `index.html` is at the root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, then save.
5. Open the published URL shown in Settings → Pages after deployment completes.

## Add a new tool
1. Create `tools/my-new-tool/`.
2. Put the main HTML file there as `index.html`; include any CSS, JavaScript, images, and other assets it needs.
3. Add an object to `tools.json`:

```json
{
  "name": "My New Tool",
  "slug": "my-new-tool",
  "category": "General",
  "description": "A short description of what the tool does.",
  "icon": "✦",
  "tags": ["keyword", "another keyword"]
}
```

The `slug` must match the folder name exactly. Search matches names, descriptions, categories, and tags. Press `/` to focus search and `Esc` to clear it. All tools include a link back to the directory. Some original tools use external CDN libraries and need an internet connection for those features.
