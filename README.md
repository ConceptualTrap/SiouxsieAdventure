# Siouxsie's Toy Hunt

A painterly autumn side-scroller starring Siouxsie, a scruffy terrier who has caught the scent of her favorite stuffed toy.

Hop the logs, leap the creeks, chase squirrels up their trees, bark the geese off the path, sniff out buried bones, and claim the prize (which does not survive).

## What's in here

| File | Purpose |
| --- | --- |
| `index.html` | The whole game: art, animation, sound and controls. No build step. |
| `manifest.webmanifest` | Lets phones install it as a full-screen, landscape app. |
| `sw.js` | Caches the game so it opens offline after the first visit. |
| `icons/` | Home-screen icons. |

## Put it online with GitHub Pages

1. Create a new repository on GitHub and upload everything in this folder, keeping `index.html` at the top level.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, and save.
4. After a minute the game is live at `https://<your-username>.github.io/<repo-name>/`.

## Play it on a phone

Open the GitHub Pages link on your phone and hold it sideways.

- **iPhone (Safari):** tap Share → **Add to Home Screen**. It then opens full screen, like an app.
- **Android (Chrome):** tap ⋮ → **Install app** or **Add to Home screen**.

Sound starts after your first tap. On iPhone, the ring/silent switch must be off to hear game sounds. The **Sound on / off** button in the top corner (or the M key) mutes everything.

## Controls

| Action | Keyboard | Phone (landscape) |
| --- | --- | --- |
| Walk / turn around | ← → or A D | ◀ ▶ |
| Run | Keep holding a direction | Keep holding ◀ ▶ |
| Jump (hold for higher) | Space, ↑ or W | Jump |
| Sniff and dig up bones | ↓ or S | Sniff |
| Bark (shoos geese) | R | Bark |
| Sound on / off | M | Sound button |

## How it's made

Everything is generated in code on an HTML canvas, with no image or audio files. The scenery is painted at load from thousands of small brush dabs, layered with parallax and a canvas-weave paper texture. Siouxsie is a procedural rig: two-bone leg IK with walk and gallop cycles, spring-driven ears and body, a physics-chained feathery tail, and blended poses for sniffing, digging, sitting, shaking off water, barking, dancing and her proud finish. Every sound, from birdsong to goose honks to the toy's last squeak, is synthesized live with the Web Audio API.

Fonts load from Google Fonts (Young Serif, Karla, Caveat); the game falls back to system fonts offline.
