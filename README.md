# PLAY//WEB

A Netflix-style launcher for games that run in the browser. Pick a game and it opens the game's own site.

**Live:** https://web-play-six.vercel.app/game-launcher/

The game list comes from a post by [@cryptuber](https://x.com/cryptuber/status/2109519982396895375) listing AAA and classic PC games ported to the web.

## Run it

It's a single HTML file with no build step. Open `game-launcher/index.html` in a browser, or serve the folder:

```bash
python -m http.server 8765 --directory game-launcher
```

Then visit http://localhost:8765.

## Features

- Rotating featured banner, rows that scroll sideways, a Top 10 row and an A to Z poster row
- Hover previews and a details popup with "More Like This"
- Search (press `/`), My List, Continue Playing, and Play Something (opens a random game)
- Real cover art in two shapes for each game: vertical (2:3) and horizontal (16:9)
- Unverified links open a warning first instead of going straight to the site
- Works on phones

## Editing the list

Everything lives in `game-launcher/index.html`:

- `GAMES`: title, link, rows, description and title style for each game
- `ART`: artwork for each game. For a Steam game, `steam(appId)` is enough.
- `ROWS`, `TOP10` and `FEATURED`: what shows on the home page

## Notes

- Every game is hosted by a third party, and most are unofficial fan ports. This page only links to them. Don't enter passwords or payment details on any of them.
- Game artwork belongs to its publishers and is loaded from Steam, GOG, Wikipedia and the games' own sites.
- Links were last checked on Oct 16, 2026. Links that had died or been hijacked were left out; the page footer lists them.
