# Resurface

A small prototype for catalog marketing teams: type a plain-language brief, get a ranked shortlist of recordings with a stated reason and a commercial-opportunity score for each pick.

Live at **[enrichmusic.anuprao.dev](https://enrichmusic.anuprao.dev)**.

## Running it

Everything lives in `index.html` — one file, no build step, no backend, no dependencies. Double-click to open it, or serve the folder with anything (`python -m http.server`, `npx serve`, etc.).

## Deployment

Hosted on GitHub Pages from `main`. The `CNAME` file points the site at `enrichmusic.anuprao.dev`; the DNS record lives on the `anuprao.dev` zone as a CNAME to `anuprao.github.io`.

## Data

- Track metadata, artwork, streaming rank, BPM, loudness and ISRC come from the Deezer public API — 229 recordings across 71 Warner-family catalog artists.
- Mood / context / sync-brief / texture / theme tags are LLM-authored for this sample; at real scale they'd come from audio models + lyric analysis.
- Original release years were resolved by hand. Deezer returns the release date of whichever reissue is being served, so "Take on Me" comes back as 2007 and "Respect" as 1995. Fixing this matters for anniversary planning.

Not affiliated with Warner Music Group.
