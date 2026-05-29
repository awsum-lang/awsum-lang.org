# awsum-lang.org

Static website for the [Awsum](https://awsum-lang.org) programming language, hosted on GitHub Pages.

## Structure

```
static/
├── index.html      # Landing page (hero, "Why Awsum?", "Backed by" — the pitch)
├── install.html    # Install instructions (compiler + target runtimes + editor extensions)
├── docs.html       # CLI usage + links to design docs and the prelude on GitHub
├── funding.html    # Funding page (pitch + sponsor CTA)
├── catastrophes-caused-by-programming-language-defects.html
├── 404.html        # Tiny JS redirect to the canonical domain
├── CNAME           # Custom domain config
├── robots.txt      # SEO config
├── llms.txt        # LLM-facing index — links to llms-full.txt, design docs, repos
├── llms-full.txt   # Self-contained LLM reference — language, prelude API, tested example
├── favicon.svg / favicon-light.svg
├── github-logo.svg
└── fonts/          # Inter, Space Grotesk, JetBrains Mono (self-hosted woff2)
```

The shared site nav (`Install` / `Docs` / `Funding` / `Community` / GitHub icon) is duplicated by hand across `index.html`, `install.html`, `docs.html`, `funding.html`, `community.html`, and `catastrophes-...html`. When changing it, update all six. The same six files also carry a hand-duplicated footer linking `llms.txt` / `llms-full.txt` (the AI/LLM-docs pointer) — keep it in sync across all six too.

## Deployment

GitHub Pages, custom domain `awsum-lang.org`. The deploy workflow ([`.github/workflows/gh-pages.yml`](.github/workflows/gh-pages.yml)) is `workflow_dispatch` only — auto-deploy on push is deliberately off so `main` can accumulate changes without going live. The site is published from the Actions tab as part of the release window for the matching `awsum` compiler version, not before.

## Design

- Pure HTML/CSS, no build step.
- Dark / light mode via CSS `prefers-color-scheme` media queries.
- Web fonts (Inter, Space Grotesk, JetBrains Mono) self-hosted as `woff2` under [`static/fonts/`](static/fonts/) via `@font-face`.
- max-width ~1140px on desktop, single-column flow that collapses cleanly on mobile.
- Minimal JavaScript — only the install-page OS tab auto-selector (reads `navigator.userAgent`) and the 404 redirect. No frameworks, no analytics.

## Related

- Compiler: [awsum-lang/awsum](https://github.com/awsum-lang/awsum)
- VSCode extension: [awsum-lang/awsum-vscode](https://github.com/awsum-lang/awsum-vscode)
- Zed extension: [awsum-lang/awsum-zed](https://github.com/awsum-lang/awsum-zed)
- Tree-sitter grammar: [awsum-lang/tree-sitter-awsum](https://github.com/awsum-lang/tree-sitter-awsum)
- Examples: [awsum-lang/awsum-examples](https://github.com/awsum-lang/awsum-examples)

## AI use

This site is developed with substantial usage of generative AI. Every generated change is reviewed, edited, and accepted by a human before it lands in the repository, and no output is shipped unedited.

## License

Apache 2.0 — see [LICENSE](LICENSE) and [NOTICE](NOTICE).
