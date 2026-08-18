# Instructions for AI assistants working on this site

This is Paul Walton's personal blog/journal: https://pijmmy.github.io

Plain HTML/CSS. No build tool, no framework, no dependencies. Keep it that way.

## What this site is for

Paul writes drafts (often pasted from elsewhere, e.g. a docx) and wants them
polished and published with minimal friction. Treat this like helping someone
write in a journal — the AI's job is light editing help and turning the draft
into a published post, not adding process.

## Writing style

Paul admires Paul Graham's and Derek Sivers' essays — not their site layouts,
their writing. When polishing a draft, aim for that register:

- Short, plain sentences. Say the thing directly instead of building up to it.
- Ordinary words over fancy ones. Cut hedging ("I think", "sort of", "kind of")
  unless it's doing real work.
- Ideas first, personality second — no forced jokes, no filler intros, no
  "in this post I will discuss...". Just start.
- Keep his voice and actual opinions. Polishing means clarity and trimming,
  not rewriting him into a different person or inflating with adjectives.
- Short paragraphs. One idea each is fine — it doesn't need padding to feel
  complete.

## Publishing a post — the workflow

1. Paul pastes a draft into the chat.
2. Polish it together in conversation — light edits, his call on how much.
3. Copy `posts/_template.html` to `posts/<slug>.html`, fill in the date
   (e.g. `19 August 2026`), title, and the full polished content as `<p>` tags.
4. Add a matching `<article>` teaser to the top of `index.html` (most recent
   first) — same date and title, then a one- or two-sentence excerpt (usually
   the post's opening), and a "Continue reading" link:
   ```html
   <article>
     <div class="date">DD Month YYYY</div>
     <h1>Title</h1>
     <p>Excerpt — a sentence or two, not the whole post.</p>
     <a href="posts/<slug>.html" class="continue">Continue reading</a>
   </article>
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
