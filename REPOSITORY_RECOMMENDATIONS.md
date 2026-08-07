# 🚀 Master GitHub Repository & Branding Strategy Guide

**Engineer:** Bilal Tariq  
**GitHub Profile:** [github.com/bilalchannar](https://github.com/bilalchannar)  
**Profile Repository:** `bilalchannar/bilalchannar`  

---

## 1. Setting Up Your Special Profile Repository

To activate your custom README on your main GitHub profile page:

1. Create a **public** repository named exactly matching your username: **`bilalchannar`**.
2. Upload the following files directly to the root of the repository:
   - `README.md`
   - `hero-banner.svg`
3. Commit and push your changes to the `main` branch.

---

## 2. Automated Contribution Snake Workflow 🐍

To configure the Contribution Snake animation so it automatically updates every night at midnight:

1. Create `.github/workflows/snake.yml` inside your `bilalchannar` repository:

```yaml
name: Generate Contribution Snake Animation

on:
  schedule:
    - cron: "0 0 * * *" # Runs automatically every midnight
  workflow_dispatch:
  push:
    branches:
    - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 10
    
    steps:
      - name: Generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
            
      - name: Push Snake SVG to Output Branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

2. Under **Repository Settings -> Actions -> General**, ensure Workflow permissions are set to **"Read and write permissions"**.

---

## 3. Recommended Pinned Repositories Strategy

GitHub lets you pin up to **6 repositories**. To present maximum engineering competence to recruiters, pin your repos in this exact order:

| Pin Order | Repository Name | Primary Domain | Essential GitHub Topics |
| :---: | :--- | :--- | :--- |
| 1️⃣ | **`TalentScanAI`** | AI & Web Backend | `ai`, `nlp`, `scikit-learn`, `flask`, `svelte`, `mongodb`, `docker`, `cosine-similarity` |
| 2️⃣ | **`Shrinkly`** | Full-Stack MERN | `mern-stack`, `react`, `nodejs`, `express`, `jwt`, `chartjs`, `rate-limiting`, `cron` |
| 3️⃣ | **`Muhafiz`** | Mobile Engineering | `flutter`, `dart`, `firebase`, `google-maps`, `express`, `whatsapp-bot`, `mobile-app` |
| 4️⃣ | **`HousePricePrediction`** | Data Science & ML | `machine-learning`, `python`, `selenium`, `pandas`, `scikit-learn`, `regression` |

---

## 4. Standard Repository Folder Structure

For every project repository on your profile, maintain a consistent professional folder structure:

```
project-root/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md
│   │   └── feature_request.md
│   ├── PULL_REQUEST_TEMPLATE.md
│   └── workflows/
│       └── ci.yml
├── docs/
│   ├── architecture.png
│   └── api-spec.md
├── src/ (or lib/ for Flutter)
├── tests/
├── .gitignore
├── Dockerfile / docker-compose.yml
├── LICENSE
└── README.md
```

---

## 5. Branching & Commit Message Conventions

### Branch Naming Convention
- `feature/description` (e.g., `feature/jwt-auth-middleware`)
- `bugfix/description` (e.g., `bugfix/pdf-text-parser-null-check`)
- `hotfix/description` (e.g., `hotfix/rate-limiter-header`)
- `docs/description` (e.g., `docs/update-architecture-diagram`)

### Conventional Commit Standard
Follow the **Conventional Commits** standard for clean Git history:

- `feat: add PDF resume extraction pipeline`
- `fix: resolve rate limiter memory leak on Express server`
- `docs: add API documentation for auth endpoints`
- `style: format Flutter widget tree according to dartfmt`
- `refactor: optimize Cosine Similarity computation in Flask`
- `test: add unit tests for JWT verification middleware`

---

## 6. GitHub Issue & PR Templates

### Pull Request Template (`.github/PULL_REQUEST_TEMPLATE.md`)
```markdown
## 📝 Description
Brief summary of the changes introduced in this PR.

## 🛠️ Type of Change
- [ ] Bug fix (non-breaking change fixing an issue)
- [ ] New feature (non-breaking change adding functionality)
- [ ] Refactor / Performance optimization
- [ ] Documentation update

## 🧪 How Has This Been Tested?
- [ ] Automated Unit Tests
- [ ] Manual API / UI Testing

## 📸 Screenshots / Diagrams (If applicable)
[Attach images or flowcharts here]
```

---

## 7. Versioning & Release Strategy

Use **Semantic Versioning (SemVer)** for repository releases (`vMAJOR.MINOR.PATCH`):
- `v1.0.0` — Initial production release.
- `v1.1.0` — New feature added without breaking existing API routes.
- `v1.0.1` — Backward-compatible bug fix.

---

## 8. Summary of All Generated Artifacts

- 📄 **`D:\Downloads\README.md`** — Production-ready 10/10 GitHub profile README.
- 🎨 **`D:\Downloads\hero-banner.svg`** — High-end Vercel/Linear style responsive header graphic.
- 📘 **`D:\Downloads\REPOSITORY_RECOMMENDATIONS.md`** — Repository configuration, branching, and workflow guide.
