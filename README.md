# Customer Success AI Working Group: showcase and hosting demo

This repository hosts the materials from the AI Working Group showcase: a branded presentation and a one page guide to hosting HTML products on GitHub Pages. It also serves as a live example of the pattern itself, build a product in Claude, host it here, and share one link.

## What is in this repository

| Piece | Path | What it is |
| --- | --- | --- |
| Landing page | `/index.html` | Home page linking to the showcase and hosting steps |
| The showcase | `/showcase/` | Branded slide style presentation given to the AI Working Group |
| Hosting steps | `/hosting-steps/` | One page guide to hosting an HTML product on GitHub Pages |
| Branding with Claude | `/branding/` | Workflow for consistent on-brand HTML and PowerPoint from Claude |
| Brand fonts | `/fonts/` | The six Elsevier web fonts (woff2), referenced by relative paths |

## Live site

Served from the address shown in `Settings > Pages`. Replace the base below with your actual Pages URL if it differs.

- Home: `https://mcguireaels.github.io/CSAIWORKING-Hosting/`
- Showcase: `https://mcguireaels.github.io/CSAIWORKING-Hosting/showcase/`
- Hosting steps: `https://mcguireaels.github.io/CSAIWORKING-Hosting/hosting-steps/`
- Branding guidance: `https://mcguireaels.github.io/CSAIWORKING-Hosting/branding/`

## Repository layout

```
/
|- index.html            landing page linking to the pages
|- README.md             this file
|- showcase/
|  |- index.html         the presentation
|- hosting-steps/
|  |- index.html         the hosting one pager
|- branding/
|  |- index.html         the branding reference
|- fonts/
   |- tiempos-text-regular.woff2
   |- tiempos-text-regular-italic.woff2
   |- national-2-regular.woff2
   |- national-2-regular-italic.woff2
   |- national-2-bold.woff2
   |- national-2-bold-italic.woff2
```

## Host an HTML product on GitHub Pages

The reusable pattern: build a product in Claude, host it here, share one link, and optionally measure how it gets used.

1. **Create a repository.** Click `New`, name it clearly, and set it to Public (Pages needs public on our plan).
2. **Add your files.** Use `Add file > Upload files`, drag in your `index.html`, and include a `fonts` folder if you use the brand fonts. Commit the changes.
3. **Turn on Pages.** Go to `Settings > Pages`. Under Source choose `Deploy from a branch`, set the branch to `main` and the folder to `/ (root)`, then Save.
4. **Get your link.** Wait about a minute and refresh. A box reads "Your site is live at ..." with the full URL. That is your shareable address.
5. **Update anytime.** Edit or re-upload the file and commit. Within a minute the same link serves the new version, so nobody is holding a stale copy.

## Worth knowing

- The entry file must be named `index.html` to load at a folder root. Each subfolder page needs its own `index.html`.
- Public repositories only, unless paid. Do not put anything confidential in a public repo.
- Give the first deploy a minute. If the live link 404s immediately, wait and hard refresh.
- Fonts live in `/fonts` and are referenced with relative paths, so the folder must travel with the HTML.
- Static hosting is for self contained pages, not apps that need a database or a login.

## Brand fonts

The two families are Tiempos Text (serif, headlines) and National 2 (sans serif, body and UI). They are provided as woff2 web fonts in `/fonts`, wired with `@font-face` and relative paths. Public hosting of these files is cleared by brand and legal. The sanctioned fallback stacks are Georgia for the serif and Arial for the sans serif.

## Note on the logo

The page headers currently show a placeholder text wordmark. Swap in the official Elsevier logo and Non Solus mark before any external use.
