# Paul Walton's site

Plain HTML/CSS, no build tool, no dependencies.

## Writing a new post

1. Copy `posts/_template.html` to `posts/your-slug.html`.
2. Fill in the title, date, and content.
3. Add a line to the list in `index.html`:

   ```html
   <li><time datetime="YYYY-MM-DD">DD Mon YYYY</time> <a href="posts/your-slug.html">Your Title</a></li>
   ```

   Add new entries at the top of the list (most recent first).

## Publishing (GitHub Pages)

1. Create a GitHub repo named `<your-github-username>.github.io`.
2. Push this folder's contents to the `main` branch.
3. In the repo Settings → Pages, set source to `main` / root (usually auto-detected).
4. Site is live at `https://<your-github-username>.github.io`.

To publish a new post: edit/add files, commit, push. No build step.
