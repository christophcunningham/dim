# DIM

Open a floor plan or shop drawing, set its scale, and take quick measurements in the browser.

**Measure**, **Layout** and **Shop drawing** work today. The **Cut** and **Print** modes are previews of what the tool could grow into: pictures only, not working yet.

## Measure

- **Open a PDF, an image or a `.dim` project.** Use the button or drop a file onto the canvas. Multi-page PDFs get Prev/Next page buttons.
- **Set the scale** in one of two ways:
  - Pick the scale printed on the sheet: architectural (3/32" to 3" = 1'-0"), engineering (1" = 10' to 100') or ratio (1:1, 1:2, 1:4, 1:5, 1:8, 1:10, 1:20 to 1:200). This only works when the PDF is at its true sheet size, which plotted CAD PDFs usually are.
  - **Calibrate:** click both ends of a dimension you know (a door, a dimensioned wall) and type its real length in inches: `144`, `36 1/2` or `150.25` (`12'-0"` and `3.2 m` work too). Scans and photos have no true size, so they always need this.
- **Snap to the drawing:** DIM reads the vector lines in a PDF, so points lock onto line ends (preferred) or onto a line. Hold Alt to place a point without snapping. Scans and images have no lines to snap to.
- **Photos and site surveys:** the **Dimension** tool (`D`) draws a dimension line on a photo; type the size you measured (`48 1/2`, `8'-2 1/2"`) and it shows on the line. Lengths, runs and areas can also take a typed size or label instead of the measured value. Export the marked-up photo as a JPG or PDF.
- **Opening a file:** DIM starts empty; use **Open file** or drop a file on the canvas. **Sample plan** in the Drawing panel loads a sample. Files start on Length (Dimension for photos), not Scale.
- **Tools:** Length, Run (several segments), Curve (`K`: click points along it; 3 points make a true arc and show its radius, more points follow any curve), Area, Rectangle area (two corners), Count (click each item; Enter starts a new count), Angle (three clicks, corner in the middle) and Note (pin a note, type it in the list; rotate the text or flip it upside down).
- **Color and ends:** the selected measurement can take any color, and its points can show as squares, dots, arrows, ticks, slashes or nothing. New measurements use the last color and ends you picked.
- **Edit** (`V`): drag points (rectangles stay rectangular); right-click any point to remove it, or the last point while drawing; Delete removes the selection; arrow keys nudge it (Shift for 10×); double-click an edge to add a point.
- **On the selected measurement:** a category (Mural, Privacy film, Distraction markers, Signage) that Layout uses when it imports from Measure, and **Deduct** for areas such as doors and windows. Totals use typed sizes where you entered them, and show area, deductions and net area, counts, and subtotals per category.
- **Undo / redo** with Ctrl+Z and Ctrl+Shift+Z (Cmd on a Mac), or the buttons in the top bar. Covers Measure and Layout.
- **in / ft-in** in the status bar switches how lengths are shown. Inches is the default.

## Shop drawing

One sheet, ready to send for approval: the drawing, a title block, your logo and a scale bar.

- **Sheet:** Letter (8.5 × 11), Tabloid (11 × 17, the default), Arch C (18 × 24) or Arch D (24 × 36), landscape or portrait. A thin black border runs around the sheet.
- **Drawing:** the Measure drawing with its measurements (the whole page, or framed around the measurements), or any Layout job (mural, privacy film, distraction markers). Fit it to the frame or pick a scale such as 1/4" = 1'-0"; the hand tool (`H`) slides it in its frame. Layout's **Open as shop drawing** button jumps here with that job.
- **Title block:** client name, project name, project location, date, sheet number and drawing title, plus your **company logo** (any image; DIM remembers it in this browser for the next job). The **scale bar** sits in the bottom right and can be turned off.
- **Text and shapes:** text boxes (size, bold, alignment, color), rectangles, ellipses, lines and arrows, with outline and fill colors, line width and dashes. Click to drop one, or drag to size it; Shift keeps lines straight; drag the corner handles to resize; Delete removes; arrow keys nudge.
- **Export PDF:** a true-size PDF. The drawing prints at up to 300 ppi; the title block, text and shapes are vector, so they stay sharp.

## Projects and exports

- **Save project (.dim)** (or Ctrl+S): one file with the drawing, scales, measurements and Layout settings (including a mural image). Send it to a coworker; they open it with the same Open button.
- **Autosave:** DIM keeps the current project in the browser, so a refresh or closed tab picks up where you left off. A private window may not keep it.
- **Marked-up PDF:** your measurements drawn on the original sheet (vector, on top of the architect's PDF), plus a list page with totals.
- **Marked-up image (JPG):** the drawing or photo with your measurements burned in, at full photo resolution, easy to text or email.
- **Copy list** and **CSV** (with category, value, unit and inches).

## Layout

Plain numbers are inches; `24'`, `2'-6"` and `3.2 m` work too. Roll widths: 48", 54", 60" and 61". **Printer margin** (default 6", both edges together) sets the printable width, so a 54" roll prints 48" wide; murals and film are laid out on the printable width, and media used is counted on the full roll.

- **Mural:** wall width and height (or a rectangle or length from Measure), bleed on each edge (default 1"), overlap between panels (default 1"), drops or rows, and all panels equal (the default) or full rolls with a trimmed last panel. **Drag a seam** on the preview to move it off a face or logo; later seams slide with it and the last panel takes up the difference. Fill with a solid color, a gradient or an image (fill, fit, stretch or a repeating pattern). Exports **panels as a true-size PDF** (one page per panel, with optional labels and seam marks in the bleed), a zip of PNG tiles, a panel map, a panel list and a CSV.
- **Privacy film:** glass panes (width, height, quantity) with a bleed on each edge, laid out as drops or rows, whichever uses less film. **Add from Measure** turns rectangles and lengths (tagged Privacy film, or untagged) into panes. Totals **glass area in sq ft** by default, or **linear feet of glass** (horizontal width × quantity), plus roll used, film area, seams and yield; the quote can charge by glass area, linear feet or film used.
- **Distraction markers:** glass runs, band heights (bottom edge from the floor, e.g. `30, 60`), band height and pattern (squares, dots or a solid line). **Add from Measure** brings in lengths and runs. **Cut file (PDF or SVG):** pieces nested across the roll at true size, cut lines on a spot color named CutContour (PDF pages up to 10 ft; long strips split at the longest strip you set).
- **Quote** (each job): price and install rate per sq ft or LF, setup, minimum, rush, and what to charge on. Copy the quote into an email or PressWise. Prices are examples until you change them; DIM remembers yours in the browser.

**Privacy:** files open on your own device and are never uploaded. Autosave stays in this browser only.

**Accuracy:** always check the scale by measuring a dimension that's printed on the sheet. Values are shown to the nearest 1/8".

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The whole app: page, styles and script |
| `vendor/pdfjs/` | Mozilla pdf.js 3.11.174, which draws the PDFs (Apache-2.0, license included) |
| `vendor/pdf-lib/` | pdf-lib 1.17.1, which writes the marked-up and panel PDFs (MIT, license included) |
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
- **Colors:** Runebender's gray theme (`assets/themes/default/gray.theme.toml` in runebender-xilem): ten gray stops, its rainbow mark colors, 10px panel corners, 1px dark outlines and filled points.
