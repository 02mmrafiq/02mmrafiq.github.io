# Mubeen — Portfolio

A single-page portfolio for Mubeen (data analyst). Built on the **Dimension** template by
[HTML5 UP](https://html5up.net) (free under the CCA 3.0 licence), recoloured to the **Solid State**
palette, with a Binnie-style projects grid.

- **Layout:** Dimension — full-screen background, centred header, panels that fade in on click.
- **Colours:** Solid State — base `#2e3141`, indigo accent `#4c5c96`, white text.
- **Tabs:** About · Projects · CV · Contact.

---

## Everything placeholder — what to fill in

All the text and images are dummy content. Open `index.html` and search for **`EDIT:`** — every
comment marks a spot to change. Quick checklist:

| What | Where |
|------|-------|
| Full name + tagline | `index.html` header (search `EDIT: Mubeen's full name`) |
| About copy | `#about` article |
| Projects (title, category, blurb, thumbnail) | `#projects` grid — one `<a class="project-card">` per project |
| Project detail pages | `projects/*.html` (case-study copy) |
| Skills / experience / education | `#cv` article |
| CV PDF | add `assets/files/mubeen-cv.pdf` (see below) |
| Email, LinkedIn, GitHub links | `#contact` icons (search `EDIT: real links`) |
| Footer name/year | `#footer` |

### Images
Swap the files in `/images` (keep the same names) or point the `src` / `background-image` at new ones:
- `pic01–03.jpg` — About photo + project thumbnails
- `bg.jpg` — the full-screen background (an indigo tint is applied over it automatically)

### Add a real CV download
The PDF lives at `assets/files/mubeen-cv.pdf` and the CV button points there. To update it, drop a
new file in over the top keeping the same name.

### Make the contact form actually send
The form is inert until wired to a backend. Easiest option — [Formspree](https://formspree.io):
1. Sign up, create a form, copy its endpoint.
2. In `index.html` `#contact`, set `action="https://formspree.io/f/XXXX"` and `method="POST"`.

(Or delete the form and rely on the email button.)

---

## Editing this with Claude (easiest option)
Alongside this folder you were sent `CLAUDE.md`, a briefing that explains how the site is put
together. Open the folder **containing** this one in Claude (Claude Code or Cowork) and it reads
that briefing automatically. It is kept outside this folder deliberately, so it never ends up in
the public repo. Then just ask in plain English:

- *"Put my real bio in the About section"*
- *"Add a new project about my customer churn analysis"*
- *"Swap the background image for this one"*
- *"Publish my latest changes"*

You don't need to touch the files yourself unless you want to — describe the change and let Claude
make it, then preview.

---

## Adding a new project
1. Copy `projects/loan-defaults.html` to `projects/your-project.html` and edit the copy.
2. In `index.html`, duplicate a `<a class="project-card">` block in the `#projects` grid and point its
   `href` at your new page.

---

## Deploy to GitHub Pages
1. Create a repo (e.g. `mobeen-portfolio`) and push these files to the `main` branch.
2. Repo → **Settings → Pages** → Source: **Deploy from a branch** → Branch: **main**, folder **/ (root)** → Save.
3. Live in ~1 min at `https://<username>.github.io/mobeen-portfolio/`.
   For a bare `https://<username>.github.io/`, name the repo `<username>.github.io` instead.

```bash
git init
git add .
git commit -m "Mubeen portfolio"
git branch -M main
git remote add origin https://github.com/<username>/mobeen-portfolio.git
git push -u origin main
```

---

## Licence note (please keep)
The Dimension template is free under [CCA 3.0](https://html5up.net/license), which **requires keeping
the credit** to HTML5 UP. It's the small `Design: HTML5 UP` line in the footer — leave it in.
Everything else is yours to change.
