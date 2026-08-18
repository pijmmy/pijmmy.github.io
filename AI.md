# Instructions for AI assistants working on this site

This is Paul Walton's personal blog/journal: https://pijmmy.github.io

Plain HTML/CSS. No build tool, no framework, no dependencies. Keep it that way.

## What this site is for

Paul writes drafts (often pasted from elsewhere, e.g. a docx) and wants them
polished and published with minimal friction. Treat this like helping someone
write in a journal — the AI's job is light editing help and turning the draft
into a published post, not adding process.

## Publishing a post — the workflow

1. Paul pastes a draft into the chat.
2. Polish it together in conversation — light edits, his call on how much.
3. Copy `posts/_template.html` to `posts/<slug>.html`, fill in title, date
   (`YYYY-MM-DD` in `<time datetime>`, human-readable in the visible text),
   and the polished content as `<p>` tags.
4. Add one `<li>` to the top of the list in `index.html` (most recent first):
   ```html
   <li><time datetime="YYYY-MM-DD">DD Mon YYYY</time> <a href="posts/<slug>.html">Title</a></li>
   ```
5. **Ask Paul for confirmation before publishing** — do not auto-push.
   Once he confirms, commit and `git push` to `main`. GitHub Pages serves
   straight from `main` at the repo root — no build step, so it's live
   within a minute of pushing.

## Rules

- Do not add a build tool, static site generator, JS framework, or CMS.
  If asked to make writing easier, prefer improving this plain-HTML workflow
  over introducing new tooling.
- Do not restyle or redesign `style.css` without Paul explicitly asking for
  a design change — the look was chosen deliberately (minimal, serif,
  Paul Graham / Derek Sivers style).
- Keep new posts consistent with the structure in `posts/_template.html`.
- Never push to `main` (i.e. publish) without explicit confirmation in the
  same conversation, even if a previous post was approved.
- Repo: github.com/pijmmy/pijmmy.github.io — public, live at pijmmy.github.io.
