# Navid Khazaee — CV (LaTeX / Overleaf)

## How to compile
1. Upload **all files** (this folder's contents) to an Overleaf project.
2. Set the compiler to **XeLaTeX** (Menu → Compiler → XeLaTeX).
3. Compile `main.tex`.

---

## Project structure

```
main.tex                  ← compile this
config/
  colors.tex              ← color palette (change myblue to retheme)
  packages.tex            ← all \usepackage declarations
  fonts.tex               ← font families & icon fonts
  layout.tex              ← geometry, macros (\cventry, \eduentry, …)
sections/
  header.tex              ← name, phone, email, social links
  experience.tex          ← work history  ← most often edited
  education.tex           ← degrees
  skills.tex              ← technical skills
  publications.tex        ← papers & conferences
  projects.tex            ← side / research projects
  teaching.tex            ← teaching & tutoring roles
  honors.tex              ← awards & achievements
  memberships.tex         ← societies & committees
  languages.tex           ← spoken languages & test scores
  certificates.tex        ← certificates & licenses
  hobbies.tex             ← personal interests
  references.tex          ← reference contacts (off by default)
  research_interests.tex  ← optional section (off by default)
fonts & assets/
  Fontin*.otf, FontAwesome.otf, ionicons.ttf, …
  me.jpg
```

---

## Toggling sections on / off

In `main.tex`, comment or uncomment the `\input{sections/...}` lines:

```latex
% \input{sections/references}     % ← uncomment to show references
```

---

## Instructions for AI agents

### Tailoring the CV for a specific job description

**Only edit files marked `[AGENT-EDITABLE]`** — these are:
- `sections/header.tex`
- `sections/experience.tex`
- `sections/skills.tex`

**Do NOT edit** `config/` files unless you are changing the overall visual style.

### Adding a new job entry

In `sections/experience.tex`, use the `\cventry` macro:

```latex
\cventry{StartYear}{EndYear or "Curr."}
  {Job Title}
  {\href{https://company.com}{Company Name}, City, Country}
  {Tech · Stack · Keywords}
  {
    \tabitem Key achievement or responsibility.
    \tabitem Another bullet point.
  }
```

### Reordering sections

Change the order of `\input{sections/...}` lines in `main.tex`.

### Highlighting skills for a role

In `sections/skills.tex`:
- Move the most relevant skills to the **Hands-on** row.
- Add new technologies to the appropriate row.
- Use `\sout{SkillName}` to visually strike through stale skills.

### Updating contact info

Edit the `sections/header.tex` file — all contact details are in one clearly marked block.

---

## Retheme the CV

Change the primary colour in `config/colors.tex`:

```latex
\definecolor{myblue}{RGB}{29,57,127}   % ← change these three numbers
```

RGB presets:
- Navy (current): `29, 57, 127`
- Forest green:   `34, 85, 34`
- Charcoal:       `50, 50, 50`
- Burgundy:       `128, 0, 32`
