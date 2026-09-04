# Deploying this repo

## 1. Push it to GitHub

```bash
cd cloud-security-devsecops-journey
git init
git add .
git commit -m "Initial scaffold: roadmap, curriculum, phase structure, Jekyll site"
git branch -M main
git remote add origin https://github.com/<your-username>/cloud-security-devsecops-journey.git
git push -u origin main
```

Create the empty repo on GitHub first (github.com → New repository), don't initialize it with a README there, or the push above will conflict.

## 2. Update two config values with your real details

Before or right after the first push, edit `_config.yml` and replace:
- `url: "https://YOUR-USERNAME.github.io"` → your actual GitHub username
- `baseurl: "/cloud-security-devsecops-journey"` → your actual repo name, if you rename it
- the `nav_external_links` GitHub URL → your actual repo URL

These only affect internal links and the "Repo on GitHub" sidebar link — the site builds fine without editing them first, but links will point at placeholders until you do.

## 3. Turn on GitHub Pages

1. On GitHub: **Settings → Pages**
2. **Source:** Deploy from a branch
3. **Branch:** `main`, folder `/ (root)`
4. Save.

GitHub Pages runs Jekyll automatically on every push — no local Ruby install, no `bundle exec`, no build step you have to run yourself. The theme (`just-the-docs`) is pulled in via `remote_theme` in `_config.yml`, which is one of GitHub Pages' officially supported plugins, so the whole thing builds server-side. You'll get a live URL like `https://<your-username>.github.io/cloud-security-devsecops-journey/` within a minute or two of the first successful build.

Check the **Actions** tab if the site doesn't appear after a few minutes — GitHub Pages builds show up there as a workflow run, and any Jekyll build error (usually a YAML front-matter typo) will show in the logs.

## 4. What's built into the site vs. what stays as plain repo files

`_config.yml` deliberately excludes some content from the Jekyll build — these stay as ordinary files, browsable on GitHub the normal way, just not part of the styled site or its sidebar:

- The repo's own `README.md` (GitHub's landing page for the repo itself — separate from the site's `index.md` homepage)
- `weekly-notes/`, `monthly-reviews/` — dated logs
- Each phase's `notes.md`, `articles.md`, `labs/`, `project/`, `evidence/` — working files and raw evidence

Everything else — `index.md`, `ROADMAP.md`, `CURRICULUM.md`, `skills-matrix.md`, and every phase's `README.md` — is a real page in the site's sidebar nav, in that order.

If you later decide you *do* want notes/articles/evidence rendered in the styled site too, remove the relevant line from `_config.yml`'s `exclude:` list and add front matter (`title:`, `parent:`, `nav_order:`) to the file the same way the phase READMEs already have it.

## 5. Optional: preview locally before pushing

Not required — GitHub builds it for you — but if you want to check a change before pushing:

```bash
gem install bundler jekyll
bundle init
echo 'gem "github-pages", group: :jekyll_plugins' >> Gemfile
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## A note on what I couldn't do for you

I don't have a connected tool that can create a GitHub repo or push commits on your behalf, and my sandbox has no outbound network access for a direct `git push` either. Everything above is copy-paste — genuinely a few minutes once you've created the empty repo on GitHub's side and swapped in your username.
