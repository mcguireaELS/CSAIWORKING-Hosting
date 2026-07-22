# HTML Product Hosting — Team Template

A ready-to-use starting point for publishing self-contained HTML products (interactive learning pieces, demos, prototypes — often coded with Claude) to a free, public web address using **GitHub Pages**.

Copy this repo, drop in your HTML, flip one switch, and you have a live link you can share.

> **Maintainers:** Replace the bracketed placeholders below — `[our-org]`, `[#team-channel]`, contact names — with your team's real values before circulating this template.

---

## What this is (the 30-second version)

GitHub does two jobs for us here:

1. **Filing cabinet** — a *repository* stores your files and keeps a full history of every change.
2. **Web server** — *GitHub Pages* takes those files and publishes them to the internet, for free, over HTTPS.

An HTML product from Claude is a **static** file: it runs entirely in the visitor's browser with no server behind it. That's exactly what GitHub Pages is built to serve, which is why this whole process is so light. There's nothing to install and nothing to run.

If a project needs a login, a database, or server-side logic, this is the wrong tool. For a single interactive HTML file, it's the right one.

---

## Quick start

### 1. Create your own repo from this template

Click the green **Use this template** button at the top of this page → **Create a new repository**.

- Owner: **`[our-org]`** (keep team products under the shared org, not a personal account)
- Name: use our convention — **`[project]-[short-descriptor]`**, lowercase, hyphenated (e.g. `ai-course-literacy-checklist`)
- Visibility: **Public** (required for free Pages hosting)

### 2. Add your HTML file

Replace the sample `index.html` in your new repo with your own file.

- **The main file must be named `index.html`.** This is what Pages serves by default. Nothing else in this process matters more.
- Easiest path: in your repo, click **Add file → Upload files**, drag your file in, and commit. (Prefer a visual app? GitHub Desktop works too — no command line required.)
- Put any supporting files (images, extra pages) in the same repo.

### 3. Turn on GitHub Pages

Pages is a per-repo setting and **does not carry over from the template** — you have to enable it on your new repo.

1. Open the **Settings** tab.
2. Select **Pages** from the left-hand menu.
3. Under **Source**, choose **Deploy from a branch**.
4. Select the **main** branch and the **/ (root)** folder, then click **Save**.

### 4. Get your link

Wait a minute or two, then refresh the Pages settings screen. Your live URL appears there:

```
https://[our-org].github.io/[your-repo-name]
```

That's the link you share. Every time you upload a changed file, the site updates on its own within a minute or two.

---

## Working with Claude-generated HTML

A few things behave differently once an HTML file leaves the Claude app and lives on the open web. Build these into your habits:

- **Ask Claude for a single, self-contained `.html` file.** One file with the CSS and JavaScript inline works perfectly. A React/JSX component does **not** host as-is — it needs a build step and a more involved workflow. When in doubt, request self-contained HTML.
- **Remove the in-app storage API.** If the piece used Claude's built-in persistent storage (`window.storage`), that only works inside the Claude app and will fail here. Ask Claude to swap it for standard browser storage or in-page state.
- **Standard `localStorage` works here (and only here).** It's blocked inside the Claude app but functions normally once hosted, because the page is now a regular website.
- **Keep dependencies inline where possible.** If the file loads a library from an external CDN, that resource has to stay reachable for the page to work. Fully self-contained files are the most durable.

---

## Rules of the road

- **Public means public.** The repo and the published site are visible to anyone with the link. Fine for external/marketing material. **Never** put proprietary code, internal-only content, or any patient data / PHI in anything hosted this way.
- **Use the shared org and the naming convention.** It keeps ownership with the team (not an individual who might move on) and makes URLs predictable.
- **One product per repo** unless there's a reason to group them. Keeps links clean and permissions simple.

---

## Troubleshooting

| Symptom | Most likely cause |
|---|---|
| Link shows a **404** | The main file isn't named `index.html`, or Pages hasn't finished its first deploy — wait a couple of minutes and refresh. |
| **Blank page** or broken layout | An external CDN dependency isn't loading, or the file used `window.storage`. Check the browser console (right-click → Inspect → Console). |
| **Changes aren't showing** | Give it 1–2 minutes; then hard-refresh (Ctrl/Cmd + Shift + R) to clear the browser cache. |
| **No Pages option / can't publish** | The repo may be private, or org policy restricts Pages. Check visibility, then ask an org admin. |

---

## Getting help

- Post in **`[#team-channel]`** with your repo link and a screenshot.
- Point of contact: **`[name / role]`**.
- GitHub's own beginner walkthrough: <https://github.blog/developer-skills/github/github-for-beginners-getting-started-with-github-pages/>
