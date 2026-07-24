# Claude Code — Rename pages: About becomes homepage, Timeline gets its own file

## What to do

Currently the site has: index.html (Timeline), about.html (About), bio.html (Bio).
The goal: About should be the homepage (index.html), Timeline moves to timeline.html.

## Steps

### 1. Rename files
- Rename `about.html` → `index.html` (overwrite the existing index.html)
- Rename `index.html` (the current Timeline page) → `timeline.html`

### 2. Update ALL nav links across all three files (index.html, timeline.html, bio.html)

Every page must use this nav, with class="current" on the correct page:

```html
<nav>
  <ul>
    <li><a href="index.html">About</a></li>
    <li><a href="timeline.html">Timeline</a></li>
    <li><a href="bio.html">Bio</a></li>
  </ul>
</nav>
```

- `index.html` (About): class="current" on the About link
- `timeline.html` (Timeline): class="current" on the Timeline link
- `bio.html` (Bio): class="current" on the Bio link

### 3. Do not change any other content
Do not change any text, styles, images, or footer content. Only the file names and nav links change.

### 4. Final check
After making changes confirm:
1. `index.html` is the About page (starts with `<h1>About</h1>`, nav has About as current)
2. `timeline.html` is the Timeline page (starts with `<h1>Bernardo Almeida</h1>`, nav has Timeline as current)
3. `bio.html` nav links point to index.html and timeline.html correctly
4. The old `about.html` file no longer exists (it became index.html)
5. Give a short summary of what was changed
