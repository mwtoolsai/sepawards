# Quiz Funnel Template

A clean, single-file, multi-step quiz funnel. Vanilla HTML/CSS/JS — no build step, no dependencies, no tracking. Drop it on any static host (GitHub Pages, Netlify, Vercel, S3, your own server) and it just works.

## What's inside

- `index.html` — the entire app: layout, styles, quiz logic, and config in one file.

## Customizing it

Open `index.html` and look for the `CONFIG` object near the bottom of the file (inside the `<script>` tag). Everything user-facing lives there:

- **`brand`** — name, subtitle, logo letter, footer note.
- **`socialProof`** — top-banner text. Set to `null` to hide.
- **`questions`** — array of `{ question, options }`. Add or remove entries; the progress bar and step counter update automatically.
- **`finalScreen`** — title, description, two buttons, and the URLs they redirect to.

Color theming lives in CSS variables at the top of the `<style>` block (`--accent`, `--ink`, `--bg`, etc.). Change one line, the whole funnel updates.

## Running it locally

Just open the file in a browser:

```bash
open index.html
```

Or serve it with any static server, e.g.:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying to GitHub Pages

1. Push this folder to a GitHub repo (see the `git` commands you were given).
2. In the repo settings → **Pages**, set source to `Deploy from a branch` → `main` → `/ (root)`.
3. After ~30 seconds your site is live at `https://<your-username>.github.io/<repo-name>/`.

## What this template intentionally does NOT include

- **No fake live-counter.** The original it was structured after had a fabricated "3,000 users online" counter generated client-side. That's misleading, so it's gone. The banner text is honest static copy.
- **No prize/giveaway hook.** The final screen offers a real recommendation, not a fake gift card. Promising a prize you don't intend to deliver is deceptive marketing under FTC rules and most state consumer protection laws.
- **No third-party trademarks.** Brand name, logo letter, and copy are placeholders. Use your own brand. Don't impersonate a real retailer — that's trademark infringement and you will get a takedown notice (or worse).
- **No CPA affiliate redirect cloak.** The final-screen buttons go where you tell them to in `CONFIG.finalScreen`. Use them for your own product, your own form, or a properly disclosed affiliate link.

## License

Do whatever you want with this code — but the legal warnings above are about *use*, not the code itself, and they don't go away just because the template makes it easy.
