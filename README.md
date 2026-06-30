# Article

Our team's research blog — hosting blog posts, paper reviews, and architecture proposals related to language models, world models, and AI systems.

**Live site:** `https://YOUR-USERNAME.github.io/article/`

## How this works

This repo builds automatically via GitHub Actions every time you push to `main`. No local build step is required to publish — just add a markdown file and push.

## Adding a new post

1. Create a new file in `_posts/` named exactly:
   ```
   YYYY-MM-DD-your-title-slug.md
   ```
   Example: `2026-07-14-attention-mechanism-survey.md`

2. Add front matter at the top of the file:
   ```yaml
   ---
   layout: post
   title: "Your Post Title"
   description: "One or two sentence summary, shown in previews and search results."
   date: 2026-07-14 09:00:00 +0000
   categories: [research, llm-architecture]
   tags: [llm, transformers]
   author: "Your Name"
   ---
   ```

3. Write the post body in Markdown below the front matter.

4. Commit and push to `main`. Check the **Actions** tab to watch the build; the site updates within 1–2 minutes of a successful build.

## Local preview (optional)

If you want to preview before pushing:

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000/article/` in a browser.

## Repo structure

```
article/
├── _config.yml          # site settings, theme config
├── _posts/               # all blog/paper posts (dated filenames)
├── _tabs/                # nav tabs (about, categories, tags, archives)
├── assets/img/           # images used in posts
├── .github/workflows/    # auto-deploy GitHub Actions workflow
├── Gemfile               # Ruby gem dependencies (Chirpy theme)
└── README.md
```

## Theme

This site uses [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy) via `remote_theme`, so no manual theme installation is needed — GitHub Pages builds it automatically through the included Actions workflow.

## First-time setup checklist

- [ ] Replace `YOUR-USERNAME` in `_config.yml`, `_tabs/about.md`, and this README with your actual GitHub username/org
- [ ] In repo Settings → Pages → Source, select **GitHub Actions** (not "Deploy from a branch")
- [ ] Push to `main` and check the Actions tab for the first build
- [ ] Visit `https://YOUR-USERNAME.github.io/article/` once the build succeeds
