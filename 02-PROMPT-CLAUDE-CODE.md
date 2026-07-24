# Claude Code — Reduce footer spacing on about page

In `style.css`, find the footer rule:

```
footer {
  max-width: var(--max-width);
  margin: 48px auto 0;
  padding: 24px 24px 48px;
  border-top: 1px solid var(--border);
  font-size: 15px;
  color: var(--text);
}
```

Replace `margin: 48px auto 0;` with `margin: 20px auto 0;`

Do not touch any other file or rule.
