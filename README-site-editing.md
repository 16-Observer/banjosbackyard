How to update Banjo's Backyard Farm site

Quick: edit or add Markdown files in the content/ folder, then run Hugo and push to Git.

1) Add content
- Home: content/_index.md
- About: content/about/_index.md
- Contact: content/contact/_index.md
- Products: content/products/_index.md

2) Add images
- Put images in static/images/ and reference /images/yourfile.png in Markdown or layouts.

3) Build and preview locally
- From the repo root: `hugo server -D` to preview locally at http://localhost:1313
- To build static files: `hugo --minify` (this creates/updates public/)

4) Deploy
- Commit and push to the main branch. CloudShare pulls from this repo and deploys automatically.

Contact form
- Current contact form uses Formspree. To enable it, sign up at https://formspree.io, create a form endpoint and replace the action attribute in content/contact/_index.md.

If you want, I can add a GitHub Action to auto-build the public/ folder so you don't have to commit generated files.