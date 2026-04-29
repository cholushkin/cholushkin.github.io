# 📰 Blog

A minimal news-style blog built with Markdown, Jekyll, and GitHub Pages, enhanced with a lightweight client-side UI.

Posts are written in Markdown and organized with categories like **thoughts** and **projects**, providing a simple CMS-like workflow without a traditional backend.

## 🚀 Live Site

👉 https://cholushkin.github.io/

## ✍️ How it works

- Posts live in the `_posts/` folder as Markdown files
- Categories are defined in frontmatter
- Jekyll builds the site into static files
- A small JavaScript layer adds:
  - filtering by category
  - pagination ("load more")
  - dynamic post previews

👉 No backend required — everything runs in the browser

## 📂 Structure

```
_posts/        # blog posts (Markdown)
_layouts/      # page layouts
index.html     # homepage (dynamic UI)
about.md       # about page
cheatsheets.md # cheatsheets page
```

## 🧠 Goal

To create a simple, Git-based CMS-like blog system that is:

* easy to maintain
* fast
* flexible (static + interactive)

---

## ⚙️ Tech

* GitHub Pages (hosting)
* Jekyll (build)
* Vanilla JavaScript (client-side interactivity)
