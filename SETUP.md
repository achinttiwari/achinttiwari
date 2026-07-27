# Setup Guide — achinttiwari/achinttiwari

## 1. Repo setup
1. Create the special repo at `github.com/achinttiwari/achinttiwari` if you haven't already (name must exactly match your username).
2. Copy `README.md`, `.github/workflows/snake.yml`, and the `assets/` folder into it.
3. Push to `main`. The README will render automatically on your GitHub profile.

## 2. Enable the Battle Log (live stats)
- `github-readme-stats` and `streak-stats` work immediately — no setup needed, they pull live from your public GitHub activity via URL params.
- The **contribution snake** needs the Action to run once:
  - Go to your repo → **Actions** tab → find "Generate Contribution Snake" → click **Run workflow** manually the first time.
  - It will create an `output` branch with the generated SVGs. After that, it auto-refreshes daily via the cron schedule.
  - Make sure repo Settings → Actions → General → Workflow permissions is set to **"Read and write permissions"**, or the Action won't be able to push the `output` branch.

## 3. The hero sprite (needs your input)
I don't have image-generation access in this environment, so `assets/hero-sprite.png` is currently a placeholder reference — it won't display until you add a real file at that path.

Two ways to get it made:
**Option A — AI image generator** (Midjourney, Ideogram, Leonardo, etc.). Use a prompt like:
> "Pixel art character sprite, front-facing portrait bust, fair skin, hazel eyes, short slightly wavy black hair, light mustache, clean-shaven jaw, wearing a dark hoodie or tech-casual jacket, standing at a glowing terminal/monitor, magenta and purple neon color palette, transparent background, 16-bit retro game style, crisp pixel edges, no anti-aliasing blur"

**Option B — commission or draw it yourself** at roughly 200×260px, transparent background, exported as PNG (static) or GIF (if you want an idle-breathing loop).

Once you have the file, just drop it in `assets/hero-sprite.png` (or update the path in README.md if you name it differently) — no other changes needed.

## 4. Things to sanity-check after first push
- Some tool badges (Claude, Gemini, Antigravity via shields.io) rely on the Simple Icons library, which adds new logos over time — if any badge shows a blank/broken icon, it means that specific logo isn't in the library yet. Let me know and I'll swap it for an alternative badge style.
- GitHub caches README images aggressively — if something looks stale after an edit, hard-refresh or wait a few minutes.

## 5. Still open / optional later
- Resume link — you said skip for now, easy to add as a badge in "The Party" section whenever ready.
- Custom section-divider art (currently using capsule-render gradient bands) — can be swapped for hand-drawn pixel dividers later if you want a closer match to the RaidParty reference.
