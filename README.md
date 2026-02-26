# ZhaoLab Web

Academic lab website source for Zhao Lab, maintained with [Quarto](https://quarto.org/) and published via GitHub Pages.

Live site: `<add link>`

## Project Overview

This repository contains:
- website source content (`*.qmd`, `*.md`, styles, includes, assets)
- generated static site output for deployment (`docs/`)
- bilingual content under `zh/`

## Repository Structure

```text
.
├── _includes/            # Shared HTML fragments (header/footer/nav)
├── _quarto.yml           # Quarto project and website config
├── index.qmd             # Homepage source
├── news.md               # News page source
├── people.md             # Team page source
├── publications.md       # Publications page source
├── pi.md                 # PI page source
├── contact.md            # Contact page source
├── zh/                   # Chinese content
├── images/               # Source image assets
├── pdf/                  # Source PDF assets
├── styles.css            # Custom site style
└── docs/                 # Generated site for GitHub Pages deployment
```

## Local Development and Preview

Prerequisite: install Quarto (v1.8+ recommended).

```bash
# render full site into docs/
quarto render

# live preview in browser (with local server)
quarto preview
```

If you only want a temporary local output directory, use:

```bash
quarto render --output-dir /tmp/zhaolab-preview
```

## Deployment (GitHub Pages)

Current deployment model in this repo:
- source branch: `main`
- publish directory: `docs/`
- build mode: local Quarto render + commit generated `docs/`
- no GitHub Actions Pages workflow is configured in `.github/workflows/`

Recommended deployment flow:
1. edit source files (`*.qmd`, `*.md`, assets)
2. run `quarto render`
3. verify local preview
4. commit both source updates and `docs/` output
5. push to `main` (manual by maintainer)

## Contributing

1. Create a feature/fix branch from `main`.
2. Keep commits focused and reviewable.
3. Run local render before opening PR.
4. Do not commit local caches, logs, or secrets.

## License

License file is not currently present.

Suggested next step:
- add `LICENSE` (commonly MIT, BSD-3-Clause, or CC BY 4.0 for site content)

## Citation

If you use this repository or website content in academic work, cite it as:

```bibtex
@misc{zhaolab_web,
  title        = {ZhaoLab Web},
  author       = {Zhao Lab},
  year         = {2026},
  howpublished = {GitHub repository},
  note         = {\url{<add repository URL>}}
}
```

## Privacy and Security

- Never commit credentials (`.env`, API keys, tokens, private keys).
- Avoid committing local machine paths, private datasets, or raw logs.
- Security issues should be reported privately (see `SECURITY.md`).
