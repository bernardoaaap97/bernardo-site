# Claude Code — Site updates: About text, Timeline, Bio rename

Apply all changes below. Touch only what is specified.

---

## 1. `index.html` (About page) — update bio paragraph

Find this text in the <p class="about-text">:
  "I'm the co-founder and CFO at Clustter, which is building the seller-side infrastructure for agentic commerce"

Replace it with:
  "I co-founded and was the CFO at Clustter, a startup in the agentic commerce space"

The rest of the paragraph stays unchanged.

---

## 2. `timeline.html` — update Currently and Formerly sections

### Currently section
Replace the entire <ul> under <h2>Currently</h2> with:

```html
<ul>
  <li>Helping other entrepreneurs. Working on what's next.</li>
  <li>Alumni Mentor at Insper, supporting students with career guidance and professional development</li>
</ul>
```

### Formerly section
Add the Clustter entry as the FIRST <li> inside the <ul> under <h2>Formerly</h2>:

```html
<li><strong>Co-founder &amp; CFO</strong>, Clustter — building the seller-side infrastructure for agentic commerce</li>
```

So the Formerly list starts with Clustter, followed by the existing entries (Conta Simples, Itaú BBA, Rio Endowment, Insper).

---

## 3. Rename "Bio" to "Library" across ALL pages

In every file that contains a nav link to bio.html, change the link text from "Bio" to "Library":
- `index.html`
- `timeline.html`
- `bio.html` (also update the <title> tag to "Library — Bernardo Almeida" and the <h1> to "Library")
- `blog.html`

---

## 4. Final check

Confirm:
1. About paragraph updated in index.html
2. Currently in timeline.html has 2 items (new first item + Insper)
3. Formerly in timeline.html starts with Clustter entry
4. All nav menus show "Library" instead of "Bio"
5. bio.html title and h1 updated to "Library"

Give a short summary of changes made.
