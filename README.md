# UEFA B Coaching Portfolio — Website

A static site built with Jekyll. GitHub Pages builds this automatically — you don't need to install anything locally to publish changes.

## How to add a new page

1. Create a new `.md` file (anywhere in the repo, or inside a subfolder like `session-plans/`).
2. Give it front matter at the very top:

   ```
   ---
   layout: default
   title: Your Page Title
   eyebrow: Optional small label above the title
   lede: Optional italic intro line under the title
   permalink: /your-page-url/
   ---
   ```

3. Write the page content in normal markdown below the `---`.
4. If you want it in the top navigation, add it to `_data/nav.yml`:

   ```yaml
   - title: Your Page Title
     url: /your-page-url/
   ```

5. Commit and push. GitHub rebuilds the site automatically — usually live within a minute or two.

## Diagrams

To embed one of the existing SVG diagrams, paste the raw `<svg>...</svg>` code into the markdown file inside a `<div class="diagram-wrap">...</div>`, and add a `<p class="diagram-caption">...</p>` underneath. See `dynamic-spaces.md` or `principles-of-play.md` for a working example.

## Deploying for the first time

1. Create a new **public** repository on GitHub (e.g. `uefa-b-portfolio`).
2. Push everything in this folder to that repo's `main` branch.
3. In the repo on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main / (root)**.
4. Save. GitHub gives you a URL like `https://yourusername.github.io/uefa-b-portfolio/` — that's the live site.
5. Every future push to `main` rebuilds it automatically.

## Local preview (optional)

Not required — GitHub does the building for you. If you do want to preview locally before pushing, you'd need Ruby and Jekyll installed (`bundle exec jekyll serve`), but this is entirely optional.

## Content still to add

- `coaching-philosophy.md` is a placeholder — the source document hasn't been supplied yet.
- The four session-plan pages are freshly drafted for this site (grounded in your Thin/Thick/Full framework) rather than recovered from an original file — the exact originals aren't in this project's materials. Worth a read-through to confirm they match what you actually ran.
- Only one diagram is embedded per illustrated page so far (as a working example) — more can be pasted in following the same pattern.
