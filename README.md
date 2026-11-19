# AUSPICE project website

Source for the AUSPICE website, built with [Quarto](https://quarto.org) and published free on GitHub Pages.
Every change pushed to the `main` branch rebuilds and republishes the site automatically, usually within 1–2 minutes.

## One-time setup

1. Create a new **public** repository on GitHub, e.g. `auspice` (personal account or an organisation).
2. Upload the contents of this folder to it. Using git:
   ```bash
   git init && git add . && git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/auspice.git
   git push -u origin main
   ```
   Or use **Add file → Upload files** on the GitHub website and drag in everything,
   including the hidden `.github` folder.
3. In the repository go to **Settings → Pages**, and under *Build and deployment → Source* choose **GitHub Actions**.
4. Go to the **Actions** tab. Re-run the "Publish site" workflow if it ran before step 3.
   When it finishes, the site is live at `https://YOUR-USERNAME.github.io/auspice/`.
5. Optional: uncomment `site-url` in `_quarto.yml` and set it to that address.

## Writing a blog post (no software needed)

1. In the repository on GitHub, open the `posts` folder and click **Add file → Create new file**.
2. Name it `posts/YYYY-MM-DD-short-title/index.md`. Typing the `/` creates the folders.
3. Start the file with this header, then write the post in Markdown below it:
   ```markdown
   ---
   title: "Your post title"
   description: "One-sentence summary shown on the blog page."
   author: "Your Name"
   date: 2027-01-15
   categories: [research]
   ---

   Text of the post. **Bold**, *italic*, [links](https://example.com), lists, etc.
   ```
4. To include images, upload them into the same folder as the post and write `![Caption](figure.png)`.
5. Click **Commit changes**. The post appears on the site in a minute or two.

Delete `posts/2026-11-19-welcome/` once you have real posts.

## Editing other pages

| Page | File |
|---|---|
| Project summary & goals (home page) | `index.qmd` |
| Research & publications | `publications.qmd` |
| People | `people.qmd` (instructions for photos and links are at the top of the file) |
| Footer (grant reference, contact email) | `_quarto.yml` |
| Colours & fonts | `theme.scss` |

## Previewing locally (optional)

Install Quarto from https://quarto.org/docs/get-started/, then run `quarto preview` in this folder.

## Still to do

- [ ] Replace the grant reference `NE/XXXXXXX/1` and contact email in `_quarto.yml`.
- [ ] Optionally add the official NERC/UKRI logo to the footer. Download it from UKRI's brand pages; don't recreate it.
- [ ] Replace placeholder publications.
- [ ] Add photos and profile links on the People page.
- [ ] Optional custom domain: **Settings → Pages → Custom domain**.
