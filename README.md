# Siouxsie's Adventure

A painterly autumn side-scroller starring Siouxsie, a scruffy terrier who has caught the scent of her favorite stuffed toy.

Hop the logs, leap the creeks, chase squirrels up their trees, bark the geese off the path, sniff out buried bones, leave her mark on a few spots, and claim the prize (which does not survive).

## What's in here

| File | Purpose |
| --- | --- |
| `index.html` | The whole game: art, animation, music, sound and controls. No build step. |
| `manifest.webmanifest` | Lets phones install it as a full-screen, landscape app. |
| `sw.js` | Caches the game so it opens offline after the first visit. |
| `icons/` | Home-screen icons (pixel Siouxsie). |

## Put it online with GitHub Pages

1. Create a repository on GitHub and upload everything in this folder, keeping `index.html` at the top level.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, and save.
4. After a minute the game is live at `https://<your-username>.github.io/<repo-name>/`.

To update an existing repository, upload the new files over the old ones.

## Play it on a phone

Open the link and hold the phone sideways. The controls sit in the margins either side of the game.

- **iPhone (Safari):** Share → **Add to Home Screen** opens it full screen like an app.
- **Android (Chrome):** ⋮ → **Install app** or **Add to Home screen**.

Music starts after your first tap. On iPhone the silent switch must be off to hear it.

## Controls

| Action | Keyboard | Phone (landscape) |
| --- | --- | --- |
| Walk / turn around | ← → or A D | ◀ ▶ |
| Run | Keep holding a direction | Keep holding ◀ ▶ |
| Jump (hold for higher) | Space, ↑ or W | Jump |
| Sniff (dig bones, mark spots) | ↓ or S | Sniff |
| Bark (shoos geese) | R | Bark |
| Pause | P or Esc | Pause button |
| Sound / music on or off | M / N | In the pause and title menus |

## Music

Three original songs, all sequenced live in the browser: **Cider Stand** on the title screen, **Leaf Pile Shuffle** while you play, and **Sidewalk Strut** on the ending screen.

## How it's made

Everything is generated in code, with no image or audio files. The scenery is painted at load from thousands of small brush dabs; the title screen is pixel art computed pixel by pixel. Siouxsie is a procedural rig with two-bone leg IK, walk and gallop cycles, spring-driven ears and body, and a physics-chained tail. Every sound and every note of music is synthesized with the Web Audio API.

Fonts load from Google Fonts (Young Serif, Karla, Caveat, Pixelify Sans); the game falls back to system fonts offline.
