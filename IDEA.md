---
tags:
---
# IDEA.md — نَـبَـرَ Blog Maintenance

## Project purpose
This project is for maintaining and improving Fahad’s Arabic Linux blog, **نَـبَـرَ**.

The blog publishes Arabic tutorials, guides, and technical articles about Linux. Articles are written with AI assistance and refined by Fahad before publishing.

## Important links
- Live blog: https://naba-r.dev/
- GitHub Pages URL: https://naba-r.github.io/
- GitHub repository: https://github.com/naba-r/naba-r.github.io
- Domain registrar: Porkbun
- Local repository path: /home/fahad/naba-r.github.io

## Technical stack
- Hugo v0.152.2 extended
- Custom Hugo theme: paper-custom, based on Hugo Paper
- GitHub Pages hosting
- GitHub Actions for automatic build and deployment after every push
- Obsidian with the Obsidian Git plugin for writing and managing posts
- openSUSE Tumbleweed is Fahad’s main operating system; he uses multiple operating systems

## Domain
- The GitHub repository is connected to the custom domain: https://naba-r.dev/
- The domain is managed through Porkbun
- The domain was connected to the GitHub repository on 2 April 2026
- GitHub Pages serves the site; GitHub Actions builds and deploys changes automatically

## Site structure
- Content folder: content/posts/
- Hugo configuration file: hugo.toml
- Theme location: themes/paper-custom/
- URL format: slug-only, /:title/, with no dates in URLs
- Taxonomy: tags only; no categories
- Approved tags: شروح، عن لينكس، توزيعات، برامج
- Posts are Markdown files stored in content/posts/
- Do not assume a fixed front-matter template; follow the existing posts and Fahad’s instructions

## Design
- Arabic, right-to-left (RTL) interface
- Minimal, flat, clean design
- Primary color: F28C28 (orange)
- Light orange: e67e00
- Background: faf9f6
- Title font: B Piramooz B1
- Body font: Dubai Regular
- Code font: Fira Code
- Left sidebar contains a tag cloud and the five most recent posts
- No boxes, borders, or shadows around article cards
- Single posts use a flattened design with no box background
- The “Posts” heading was removed from list pages
- The site tagline has been removed

## Publishing workflow
1. Write or edit posts in Obsidian under content/posts/
2. Commit changes:
   ```bash
   git add .
   git commit -m "Update posts"
   ```
3. Push to GitHub:
   ```bash
   git push origin main
   ```
4. GitHub Actions builds and deploys automatically, usually within 1–2 minutes
5. Verify the change at https://naba-r.dev/

## Local preview
Run Hugo locally from /home/fahad/naba-r.github.io:

```bash
hugo server --disableFastRender --ignoreCache --noHTTPCache -D
```

Then open:

```text
http://localhost:1313
```

## Git details
- Git user name: naba-r
- Git email: justwish7@gmail.com
- Main branch: main

## Files to avoid committing
```text
public/
resources/
.hugo_build.lock
.DS_Store
Thumbs.db
.obsidian/workspace.json
.obsidian/workspace-mobile.json
```

## Maintenance history
- Google Search Console ownership was verified by uploading an HTML verification file to /static/
- The sitemap was submitted to Google Search Console
- Indexing was requested for the homepage and key posts
- A separate Obsidian vault called PersonalNotes exists for non-blog personal notes
- PersonalNotes repository: https://github.com/naba-r/personal-notes.git
- On 2 April 2026, the blog repository was connected to https://naba-r.dev/ through Porkbun

## Known issues and fixes
- If CSS changes do not appear, restart Hugo with:
  ```bash
  hugo server --disableFastRender --ignoreCache --noHTTPCache -D
  ```
- If the site does not update after pushing, check the GitHub Actions tab for build errors
- If fonts do not load, verify the font path in fonts.css
- If posts do not appear, check that their dates use YYYY-MM-DD and are not in the future
- If a deployed page is blank, run:
  ```bash
  hugo list all
  ```
- Before writing in Obsidian, use “Obsidian Git: Pull” to avoid sync conflicts
- If Obsidian cannot use Git Credential Manager, use:
  ```bash
  git config --global credential.helper store
  ```
- If a merge conflict occurs in .obsidian/workspace.json or .obsidian/appearance.json, keep the local PC settings:
  ```bash
  git checkout --ours .obsidian/appearance.json .obsidian/workspace.json
  git add .
  git commit -m "Keep local Light theme settings"
  git push origin master
  ```

## Current note
The Hugo configuration may still contain:

```toml
baseURL = "[https://naba-r.github.io/](https://naba-r.github.io/)"
```

Since https://naba-r.dev/ is now the primary domain, consider updating `baseURL` to:

```toml
baseURL = "[https://naba-r.dev/](https://naba-r.dev/)"
```

This helps ensure that generated links, canonical URLs, the sitemap, and RSS feeds use the correct domain.
