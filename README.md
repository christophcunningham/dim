# DIM

Open a floor plan or shop drawing, set its scale, and take quick measurements in the browser.

DIM is a proof of concept for a shop drawing tool. **Measure** works today. The **Layout**, **Cut**, **Print** and **Shop drawing** modes are previews of what the tool could grow into: pictures only, not working yet.

## What it does

- **Open a PDF or image.** Use the button or drop a file onto the canvas. Multi-page PDFs get Prev/Next page buttons.
- **Set the scale** in one of two ways:
  - Pick the scale printed on the sheet: architectural (1/8" to 3" = 1'-0"), engineering (1" = 10' to 100') or metric (1:20 to 1:200). This only works when the PDF is at its true sheet size, which plotted CAD PDFs usually are.
  - **Calibrate:** click both ends of a dimension you know (a door, a dimensioned wall) and type its real length: `12'-0"`, `12' 6 1/2"`, `150"` or `3.2 m`. Scans and photos have no true size, so they always need this.
- **Measure:** Length, Run (several segments, e.g. a marker band along a wall) and Area (sq ft). Rename any measurement in the list.
- **Take the numbers with you:** Copy list (paste into an email or PressWise) or Download CSV.

Shortcuts: `H` pan · `S` set scale · `L` length · `R` run · `A` area · `F` fit · `+`/`-` zoom · Shift keeps lines straight · Enter or double-click finishes a run or area · Esc cancels · Backspace removes the last point · Space + drag pans · Ctrl/Cmd + scroll zooms.

**Privacy:** files are opened on your own device. Nothing is uploaded or stored, so measurements are gone when you close the tab. Copy or download them first.

**Accuracy:** always check the scale by measuring a dimension that's printed on the sheet. Values are shown to the nearest 1/8".

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The whole app: page, styles and script |
| `vendor/pdfjs/` | Mozilla pdf.js 3.11.174, which draws the PDFs (Apache-2.0, licence included) |
| `favicon.svg` | Tab icon |
| `_headers` | Security and caching headers for Cloudflare Pages |

There's no build step and nothing to install.

## Put it online (GitHub + Cloudflare Pages)

1. **Create a GitHub repository**, e.g. `dim`, and add these files at its root. You can drag them onto "uploading an existing file" on github.com, or push from your computer:

   ```bash
   git init
   git add .
   git commit -m "DIM proof of concept"
   git branch -M main
   git remote add origin https://github.com/<you>/dim.git
   git push -u origin main
   ```

2. **Connect it to Cloudflare Pages:** in the Cloudflare dashboard go to **Workers & Pages → Create → Pages → Connect to Git**, then pick the repo.
3. **Build settings:** Framework preset **None**, Build command **empty**, Build output directory **`/`**.
4. **Deploy.** You get a `dim-xxx.pages.dev` address to share. Every push to `main` redeploys.

**No GitHub?** Use **Workers & Pages → Create → Pages → Upload assets** and drag in this folder.

**Only coworkers should see it?** Put **Cloudflare Access** (Zero Trust) in front of the Pages project and allow your company's email domain. Its free plan covers small teams.

## Try it locally

pdf.js needs the page to be served, not opened as a file:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Look

- **Type:** the DIM name is set in [Lexend Zetta](https://fonts.google.com/specimen/Lexend+Zetta); everything else is [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono). Both load from Google Fonts.
- **Colours:** Runebender's gray theme (`assets/themes/default/gray.theme.toml` in runebender-xilem): ten gray stops, its rainbow mark colours, 10px panel corners, 1px dark outlines and filled points.
