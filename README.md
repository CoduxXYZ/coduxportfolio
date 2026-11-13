# Codux

A static one-page Discord portfolio (HTML, CSS and vanilla JavaScript in one file). No build step, no dependencies.

- Live Discord status, avatar badge and "Now playing" card through [Lanyard](https://github.com/Phineas/lanyard) (WebSocket, with a REST fallback).
- Click sound on the top-bar tabs (`click.ogg`, with `click.mp3` as a fallback for Safari).
- Sections: About, Experience, Projects, Lovesick (sponsored community) and Contact.

## Files

Put **all** of these in the **root** of your repository (same folder as `index.html`):

```
index.html              the whole site (HTML, CSS and JS)
FizzyBnnr.png           profile banner
kiwibot.webp            Kiwi Bot logo
ordely.webp             Ordely logo
sonarsy.webp            Sonar Systems logo
xenex.webp              Xenex logo
lovesick-banner.webp    Lovesick banner
lovesick-logo.webp      Lovesick logo
click.ogg               tab click sound
click.mp3               tab click sound (Safari fallback)
favicon.svg             browser tab icon
vercel.json             tells Vercel this is a plain static site
.gitignore  LICENSE  README.md
```

File names are case sensitive. Keep them exactly as listed.

## Put it on GitHub

1. Unzip `codux-portfolio.zip` on your computer (GitHub does not unzip for you).
2. Create a repository, then choose **Add file > Upload files**.
3. Drag in the **files** (not the zip, not a folder containing them). `index.html` must be at the top level of the repo.
4. If `.gitignore` doesn't show up in your file picker, skip it. The site works without it.
5. Commit.

## Deploy on Vercel

1. Vercel dashboard > **Add New > Project** > import your GitHub repo.
2. **Framework Preset:** `Other`. Leave Build Command, Output Directory and Install Command empty.
3. **Root Directory:** `./`. Click **Deploy**.
4. Custom domain: Project > **Settings > Domains** > add `codux.xyz`.

### If something looks wrong

| Problem | Fix |
|---|---|
| `404: NOT_FOUND` | `index.html` is not in the repo root. Move the files up, or set **Root Directory** to that folder. |
| Banner or logos missing | The image files weren't uploaded next to `index.html`, or the names don't match exactly. |
| No click sound | Make sure `click.ogg` and `click.mp3` are uploaded. Browsers only play sound after a click, which is what the tabs use. |
| Status or "Now playing" stays empty | Your Discord account must be in the Lanyard server: https://discord.gg/UrXF2cfJ7F |

## Editing

- **Discord ID for Lanyard:** `var ID='...'` at the top of the Lanyard script in `index.html`.
- **Lovesick invite:** add a button inside the `#lovesick` section once you have the link.
- **Click volume:** `snd.volume=.6` in the click-sound script at the bottom of `index.html` (0 to 1).

## License

MIT. See `LICENSE`.
