# Héctor Morales · Academic Website & Research Hub (`hectormb100.github.io`)

Personal academic website, publications, and companion research code hub for **Prof. J. Héctor Morales Bárcenas** (Departamento de Matemáticas, Universidad Autónoma Metropolitana, Unidad Iztapalapa, Mexico City).

- **Live Website:** <https://hectormb100.github.io/>
- **Papers & Code Page:** <https://hectormb100.github.io/papers.html>

## Structure

- `index.html` — Home (affiliation, research areas, scientific computing ecosystem, seminars & talks)
- `bio.html` — Biography (English, Español, Français), work experience, and education
- `research.html` — Research statement, projects, collaborators, and recorded talks
- `papers.html` — Companion code repositories, preprints, and supplementary materials for submitted papers
- `dissertations.html` — Supervised PhD, MSc, and BSc theses and internships
- `teaching.html` — Undergraduate & graduate courses at UAM Iztapalapa
- `data-science-group.html` — UAM-I Data Science Group & Divisional Seminar archive
- `papers/` — Folder for direct PDF preprints and supplementary documents (`https://hectormb100.github.io/papers/<file>.pdf`)
- `assets/` — Stylesheet (`assets/css/style.css`) and local images (`assets/images/`)

## Quick Terminal Commands

### 1. Update the website or upload a PDF document to `papers/`

```zsh
cd ~/GitHub/hectormb100.github.io
# Edit any .html file in Emacs or copy a PDF into papers/
git add .
git commit -m "Update website / add preprint"
git push
```

### 2. Publish a new companion repository when submitting a paper

Suppose your paper code is in `~/GitHub/2026-paper-name`:

```zsh
mkdir -p ~/GitHub/2026-paper-name
cd ~/GitHub/2026-paper-name
# Copy your Julia / Python / R / Stan scripts and README.md here
git init -b main
git add .
git commit -m "Initial release of simulation code for manuscript"
gh repo create hectormb100/2026-paper-name --public --source=. --remote=origin --push
```

Colleagues and reviewers can then access it directly at `https://github.com/hectormb100/2026-paper-name` (and you can link it on `papers.html`).
