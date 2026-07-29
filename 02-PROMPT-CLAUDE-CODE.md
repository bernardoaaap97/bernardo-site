# Claude Code — Fix nav on index.html and timeline.html

The Blog nav item is missing from two pages. Fix ONLY the <nav> section on these two files — do not touch anything else.

## 1. `index.html` — replace the nav with:

```html
<nav>
  <ul>
    <li><a href="index.html" class="current">About</a></li>
    <li><a href="timeline.html">Timeline</a></li>
    <li><a href="bio.html">Bio</a></li>
    <li><a href="blog.html">Blog</a></li>
  </ul>
</nav>
```

## 2. `timeline.html` — replace the nav with:

```html
<nav>
  <ul>
    <li><a href="index.html">About</a></li>
    <li><a href="timeline.html" class="current">Timeline</a></li>
    <li><a href="bio.html">Bio</a></li>
    <li><a href="blog.html">Blog</a></li>
  </ul>
</nav>
```

Do not touch bio.html, blog.html, style.css, or any other content. Only the nav on these two files.
