# SARrealists tile CDN

Web Mercator (EPSG:3857) XYZ PNG tiles for the NISAR dashboard, generated from
the COGs in Google Drive (`nisar_outputs/<site>/cog/`) with
`scripts/render_webmercator_tiles.py` in the main repository.

Layout: `/<site>/tiles_<letter>/<layer>/<date>/{z}/{x}/{y}.png`
- `california` → `tiles_c`
- `himalaya` → `tiles_h`
- `nile_delta` → `tiles_n`

Each site has a `catalog.json` listing the layers and dates that exist.

Preview zoom range: z8–11. Source resolution is 20–160 m; z11 is already
1.6–13 m/px at these latitudes, so higher zooms add no real detail from these
COGs (see `docs/TILE_PROJECTION_FINDINGS.md` in the main repo).

Served by GitHub Pages: https://mohamadadel510.github.io/SARrealists-tiles/
