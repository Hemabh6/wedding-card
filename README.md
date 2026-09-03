# Akanksha & Hemabh Aditya — wedding invitation

A single-page invitation. Scroll-driven 3D card animation, shehnai on load,
countdown to 3 December 2026.

## Files

| File | What it is |
|---|---|
| `index.html` | The page itself, 30 KB. Small enough to edit in GitHub's browser editor. |
| `card-ganesh.jpg`, `card-invite.jpg`, `card-events.jpg` | The three invitation cards. |
| `shehnai.mp3` | The shehnai, 2½ minutes from 1:30. |
| `preview.jpg` | The thumbnail WhatsApp shows when the link is shared. |

All six live side by side in the repository root. Nothing goes in folders.

## Publishing on GitHub Pages

### Through the website, no commands

1. Go to <https://github.com/new>. Name the repository something like
   `akanksha-aditya`. Set it to **Public** — Pages needs public on a free
   account. Create it.
2. On the new repository page, click **uploading an existing file**.
3. Drag in `index.html`, `shehnai.mp3` and `preview.jpg`. Click
   **Commit changes**.
4. Go to **Settings → Pages**. Under *Source* pick **Deploy from a branch**,
   choose branch `main` and folder `/ (root)`. Save.
5. Wait about a minute, then reload that page. The URL appears at the top:

       https://<your-username>.github.io/akanksha-aditya/

That link is what you send. It works on every phone, no app needed.

### Through the terminal

```bash
cd <folder containing these files>
git init -b main
git add .
git commit -m "Wedding invitation"
git remote add origin https://github.com/<your-username>/akanksha-aditya.git
git push -u origin main
```

Then do step 4 above.

## Your own domain

If you buy something like `akankshaandaditya.com`, add a file named `CNAME`
containing just that domain, then point the domain's DNS at GitHub:

    A    @    185.199.108.153
    A    @    185.199.109.153
    A    @    185.199.110.153
    A    @    185.199.111.153

Set the domain under **Settings → Pages → Custom domain** and tick
*Enforce HTTPS*.

## Changing things later

Open `index.html` in any text editor.

- **Ceremony details, names, venue, phone** — plain text in the HTML, near the
  bottom. Search for `Sangeet` or `Shagun` and edit in place.
- **The music** — the block marked `SHEHNAI` at the top of the second
  `<script>`. Setting `SHEHNAI_FILE` to another filename swaps the track.
- **Colours** — the `:root` block at the top of the stylesheet. Every colour on
  the page comes from those six values.

## One note on the recording

The shehnai is a Bismillah Khan performance, still under label copyright. For a
link shared with family and friends this is how everyone does it and nobody
minds. If this ends up somewhere public and widely indexed, swapping in a
royalty-free shehnai is a one-line change.
