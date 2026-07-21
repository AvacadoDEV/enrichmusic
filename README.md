# Resurface — catalog triage prototype

Single-file static site. `index.html` has zero dependencies and no backend: all data
and scoring logic are inline. Open it locally by double-clicking, or host it anywhere.

## Deploy to enrichmusic.anuprao.dev

**Cloudflare Pages (recommended — free, instant TLS)**
1. Push this folder to a GitHub repo.
2. Cloudflare dashboard → Workers & Pages → Create → Pages → connect the repo.
3. Build command: *none*. Build output directory: `/`.
4. After the first deploy: Custom domains → Set up a domain → `enrichmusic.anuprao.dev`.
   If `anuprao.dev` is already on Cloudflare DNS the CNAME is created for you.

**Netlify** — drag this folder onto app.netlify.com/drop, then Domain settings →
Add custom domain → `enrichmusic.anuprao.dev`, and add the CNAME it gives you at your registrar.

**GitHub Pages** — push to a repo, Settings → Pages → deploy from branch root.
The included `CNAME` file handles the custom domain; add a CNAME record at your DNS
pointing `enrichmusic` → `<username>.github.io`.

**DNS record you need either way**

    Type   Name          Value
    CNAME  enrichmusic   <your-host-target>

## Data provenance
Track metadata, artwork, streaming rank, BPM, loudness and ISRC: Deezer public API,
229 recordings across 71 Warner-family catalog artists. Mood/context/sync/texture/theme
tags are LLM-authored for this sample. Original release years were resolved manually
because the API returns reissue dates. Not affiliated with Warner Music Group.
