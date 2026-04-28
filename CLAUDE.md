# Awsum Language Website

Static website for the Awsum programming language hosted on GitHub Pages at https://awsum-lang.org

## Structure

```
static/
├── index.html    # Main landing page (inline CSS, no JS)
├── 404.html      # Redirect to main domain
├── CNAME         # Custom domain config
└── robots.txt    # SEO config
```

## Deployment

- **Hosted on**: GitHub Pages
- **Domain**: awsum-lang.org
- **Trigger**: manual only (`workflow_dispatch`). Auto-deploy on push is intentionally disabled so that `main` can accumulate changes without going live — the site goes out together with the next compiler release, not before. Run the workflow by hand from the Actions tab when the release window opens.

## Content Sections

1. Why Awsum — four key differentiators (cross-target equivalence, stack-safe recursion, honest arithmetic, compile-time platform effects)
2. Targets table (LLVM, JVM, CLR, WASM, JS) with versions
3. Editor support (VSCode)
4. Examples with links to the test-suite sources
5. Installation (compiler + per-target runtimes)
6. CLI usage documentation
7. Design documents (links to `docs/` in the compiler repo)
8. Design principles
9. Roadmap (landed vs planned)
10. Notes

## Design

- Pure HTML/CSS, no build tools
- Dark/light mode support via CSS media queries (`prefers-color-scheme`)
- Web fonts via Google Fonts (Space Grotesk for display, Inter for body, JetBrains Mono for code)
- max-width ~1140px on desktop, single-column flow that collapses cleanly on mobile
- Targeted JavaScript only — currently a small inline script for the install-section OS tabs (auto-selects from `navigator.userAgent`). No frameworks, no build step, no analytics

## Related Repositories

- Compiler: `awsum` (../awsum)
- VSCode extension: `awsum-vscode` (../awsum-vscode)
