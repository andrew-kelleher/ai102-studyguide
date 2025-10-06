# Quick Guide: Publishing Markdown with MkDocs Material on GitHub Pages

This guide helps you set up a project using [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and publish it as a GitHub Page.

---

## 1. Create a GitHub Repository

1. Go to [GitHub](https://github.com/) and create a new repository.
2. Give it a name (e.g., `my-docs-site`) and initialize it **without** a README.

---

## 2. Set Up Local Folder Structure

```bash
mkdir my-docs-site
cd my-docs-site
```

Create the following structure:

```
my-docs-site/
├── docs/
│   └── index.md
└── mkdocs.yml
```

Add content to `index.md`.

---

## 3. Install Required Python Packages

Make sure you have Python installed. Then run:

```bash
pip install mkdocs-material
```

---

## 4. Create `mkdocs.yml` Configuration

Example minimal config:

```yaml
site_name: My Docs Site
theme:
  name: material
nav:
  - Home: index.md
```

---

## 5. Preview Locally

```bash
mkdocs serve
```

Visit `http://127.0.0.1:8000` in your browser.

---

## 6. Deploy to GitHub Pages

1. Commit and push your files to GitHub:

```bash
git init
git add .
git commit -m "Initial site"
git remote add origin https://github.com/your-username/my-docs-site.git
git push -u origin main
```

2. Deploy:

```bash
mkdocs gh-deploy
```

This builds the site and pushes to the `gh-pages` branch.

---

## 7. Enable GitHub Pages

On your GitHub repo:

- Go to **Settings ▸ Pages**
- Set the source to `gh-pages` branch, root directory
- Save and your site is live!

---

**Example:** If your repo is `username/my-docs-site`, your site will be at:

```
https://username.github.io/my-docs-site/
```

---

## Optional

- Add custom domain via GitHub Pages settings
- Use a `.nojekyll` file to avoid Jekyll processing

---