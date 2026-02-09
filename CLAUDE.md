# Awsum Language Website

Static website for the Awsum programming language hosted on GitHub Pages at https://awsum-lang.org

## Structure

```
static/
├── index.html    # Main landing page (265 lines, inline CSS)
├── 404.html      # Redirect to main domain
├── CNAME         # Custom domain config
└── robots.txt    # SEO config
```

## Deployment

- **Hosted on**: GitHub Pages
- **Domain**: awsum-lang.org
- **Auto-deploy**: Push to `main` triggers GitHub Actions workflow

```bash
# Manual deployment (usually automatic via CI)
git push origin main
```

## Content Sections

1. Language overview and features
2. Compilation targets (JS, Lua)
3. Editor support (VSCode)
4. Installation instructions
5. CLI usage documentation
6. Example programs
7. Roadmap

## Design

- Pure HTML/CSS, no build tools
- Dark/light mode support via CSS media queries
- System fonts, max-width 880px
- Fully static, zero JavaScript (except 404 redirect)

## Related Repositories

- Compiler: `awsum` (../awsum)
- VSCode extension: `awsum-vscode` (../awsum-vscode)
