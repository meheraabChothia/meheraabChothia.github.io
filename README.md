# Blog Guide

## How We Set This Up

1. Created a new repo from the Chirpy starter template at `https://github.com/cotes2020/chirpy-starter`, named `meheraabChothia.github.io`
2. Cloned the repo locally
3. Installed Ruby: `sudo apt install ruby-full build-essential zlib1g-dev`
4. Configured gem path in `~/.bashrc`:
   ```
   export GEM_HOME="$HOME/gems"
   export PATH="$HOME/gems/bin:$PATH"
   ```
5. Installed Jekyll and Bundler: `gem install jekyll bundler`
6. Installed project dependencies: `bundle install`
7. On GitHub: Settings → Pages → Source → set to **GitHub Actions**

---

## Running Locally

```bash
bundle exec jekyll serve
```

Visit `http://127.0.0.1:4000` to preview.

---

## Adding a New Post

1. Create a file in `_posts/` named: `YYYY-MM-DD-your-post-title.md`
2. Add this front matter at the top:
   ```yaml
   ---
   title: Your Post Title
   date: YYYY-MM-DD
   categories: [Category1, Category2]
   tags: [tag1, tag2]
   ---
   ```
3. Write your content below the closing `---` in Markdown
4. Use `##` for top-level sections (these show in the TOC), `###` for subsections
5. Push to GitHub — the site rebuilds automatically

---

## Changing Configuration

All config lives in `_config.yml`. Key fields:

| Field | What it does |
|-------|-------------|
| `title` | Blog name |
| `tagline` | Subtitle shown under the name |
| `url` | Must be `https://meheraabChothia.github.io` |
| `avatar` | Path to sidebar profile image (e.g. `/assets/img/aquarion-1.png`) |
| `timezone` | Set to `Asia/Kolkata` |
| `github.username` | Your GitHub username |
| `social.name` | Your name shown in footer |
| `social.email` | Your email |

After any change to `_config.yml`, restart the local server to see the effect.

---

## Deploying Changes

```bash
git add .
git commit -m "your message"
git push
```

GitHub Actions handles the build and deploy. Check the **Actions** tab on your repo to monitor progress.
