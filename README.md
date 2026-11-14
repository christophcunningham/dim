# DIM

Draw at true size, open a floor plan or shop drawing, set its scale, and take quick measurements in the browser.

DIM opens on **Home**, with buttons to open a file, start a blank canvas or try the sample, and to jump to **Draw**, **Layout** or **Shop drawing**. The Home button (or the DIM logo) brings you back. The interface uses Manrope.

## Draw

- **Opens on a blank canvas** drawn at true size (1 unit = 1 inch) when nothing else is open. Open a PDF, image or `.dim` project to draw and measure over it instead.
- **Two tool sets** in the left panel, each button showing its shortcut in the corner:
  - **Draw:** Select (`V`), Pan (`H`), Line (`\`), Rectangle (`M`), Ellipse (`E`), Polyline (`P`) and Note (`T`). Line, Rectangle and Ellipse are click and drag (a click on each end works too); Shift keeps a line level or plumb and a rectangle or ellipse square or round. Polyline: click each point, Enter or double-click to finish, or click the first point to close it. Shapes have a color, a stroke (thin, regular, bold) and, when closed, a fill (none, tint, solid, white). They stay out of totals, the CSV and Layout, and only show their size when **Shape sizes** is on.
  - **Measure:** the measuring tools below. Length, Rectangle area, Circle and Dimension are click and drag too.
- **Snap grid:** on a blank canvas, **Grid** (bottom right) sets the snap size from 1/16" to 2' (1 mm to 1 m in metric; switching units moves it to the nearest size). With **Snap** on, every point lands on the grid (Alt places freely). The grid lines thin out as you zoom out and show sixteenths when you zoom in; a blank canvas zooms in far enough for that (the zoom reads as actual size, 100% = one inch per inch on screen).
- **Top left of the canvas:** undo and redo, **Grid** and **Snap** (Snap to the drawing's lines for a PDF), **Dims** (click to switch measurement tags between name and size, size only, or the selected one only), **Shape sizes**, and **Settings** (canvas size or length step, and tags).
- **Bottom right of the canvas:** the snap grid (blank canvas) or the drawing's scale (click to set it), **IN / FT-IN / MM / CM / M**, **1/16 / .001** (imperial only) and zoom.

### Measuring

- **Open a PDF, an image or a `.dim` project.** Use the button or drop a file onto the canvas. Multi-page PDFs get Prev/Next page buttons.
- **Set the scale** in one of two ways:
  - Pick the scale printed on the sheet: architectural (3/32" to 3" = 1'-0"), engineering (1" = 10' to 100') or ratio (1:1, 1:2, 1:4, 1:5, 1:8, 1:10, 1:20 to 1:200). This only works when the PDF is at its true sheet size, which plotted CAD PDFs usually are.
  - **Calibrate:** click both ends of a dimension you know (a door, a dimensioned wall) and type its real length in inches: `144`, `36 1/2` or `150.25` (`12'-0"` and `3.2 m` work too). Scans and photos have no true size, so they always need this.
- **Snap to the drawing:** DIM reads the vector lines in a PDF, so points lock onto line ends (preferred) or onto a line. Hold Alt to place a point without snapping. Scans and images have no lines to snap to.
- **Photos and site surveys:** the **Dimension** tool (`D`) draws a dimension line on a photo; type the size you measured (`48 1/2`, `8'-2 1/2"`) and it shows on the line. Lengths, runs and areas can also take a typed size or label instead of the measured value. Export the marked-up photo as a JPG or PDF.
- **Opening a file:** DIM starts empty; use **Open file** or drop a file on the canvas. **Sample plan** in the Drawing panel loads a sample, and **Blank canvas** starts an empty canvas drawn at true size (set its width and height, with an optional 1 ft grid) for mocking up shapes, where every line shows its real dimension. Files start on Length (Dimension for photos), not Scale.
- **Tools:** Length, Run (several segments), Curve (`K`: click points along it; 3 points make a true arc and show its radius, more points follow any curve), Area, Rectangle area (two corners), Count (click each item; Enter starts a new count), Angle (three clicks, corner in the middle) and Note (pin a note, type it in the list; rotate the text or flip it upside down).
- **Color and ends:** the selected measurement can take any color, and its points can show as squares, dots, arrows, ticks, slashes or nothing. New measurements use the last color and ends you picked.
- **Circle** (`O`): click the center, then the edge; shows the diameter and area.
- **Change a size from the readout:** click the big number on the left to type a new length, or width and height (Tab moves from width to height), or a diameter. Lines keep their start point; rectangles keep their first corner.
- **Snapping:** **Length step** makes clicked points land on whole 1/4" or 1" steps, so a line reads 96 1/4" instead of 96 3/16" (Drawing panel; Alt ignores it). On a blank canvas, **Snap grid** makes points stick to grid lines.
- **Tags:** measurement tags never stack. A crowded tag steps aside with a leader line, drops its name, or shrinks to a dot; select it to bring it back. Tags grow a little as you zoom in and shrink as you zoom out. **Tags on drawing** (Drawing panel) shows name and size, size only, or the selected one only. Marked-up exports and Shop drawing use the same rules.
- **Scale** (`S`): the Scale tool's panel holds the printed-scale list and known-length calibration, with the current scale in large numbers. After calibrating, the Scale tool highlights where the known length was measured.
- **Left panel:** the current tool's name and shortcut in bold, with what to do next. The status bar shows the tool, its shortcut and the scale.
- **Dimension** (`D`): hover an edge (a line of the drawing, or an edge of a measurement), then click and pull away; the dimension line and extension lines follow. Or click two points (hold Alt to ignore edges). In Edit, drag a dimension to move it closer or farther; Shift+drag moves it.
- **Reset:** **Clear measurements** (or **Reset canvas**) in the Drawing panel removes everything drawn; Undo brings it back.
- **Resize** (`Z`): select a measurement and drag a corner, or type its new length (width for areas), or scale it by a ratio (1:2, 1:4, 1:8, 1:10 smaller, or 2:1 to 10:1 larger); it scales evenly around its center. Setting the drawing's scale is its own tool (`S`).
- **Edit** (`V`): drag points (rectangles stay rectangular), or drag a line or area to move all of it; drag a curve to bend it (a 3-point arc passes through the cursor), Shift+drag to move it; right-click any point to remove it, or the last point while drawing; Delete removes the selection; arrow keys nudge it (Shift for 10×); double-click an edge to add a point.
- **On the selected measurement:** a category (Mural, Privacy film, Distraction markers, Signage) that Layout uses when it imports from Draw, and **Deduct** for areas such as doors and windows. Totals use typed sizes where you entered them, and show area, deductions and net area, counts, and subtotals per category.
- **Undo / redo** with Ctrl+Z and Ctrl+Shift+Z (Cmd on a Mac), or the buttons at the top left of the canvas (in the top bar in Layout). Covers Draw and Layout. **Cmd+0** (Ctrl+0) fits the page to the screen.
- **IN / FT-IN / MM / CM / M** (bottom right of the canvas) switches how lengths are shown; **1/16 / .001** next to it switches fractions (to 1/16") and decimals (to 0.001"). Inches and fractions are the defaults.
  - **Metric:** lengths show in mm (whole mm from 100 mm, tenths below), cm (to a tenth) or m (to the millimeter); areas in m², totals in m, and the CSV in m and m² (it keeps an Inches column). A plain number you type is in the units on screen (`1200` is 1,200 mm in MM); `48"`, `4'` or `1.2 m` always work. A new blank canvas in metric is 6 × 3.6 m with a 1 cm grid, and Length step offers 1 mm, 5 mm and 1 cm.
  - **Layout** works in inches (roll widths, film and markers), so it shows only IN / FT-IN and uses your last imperial choice while Draw is in metric. Shop drawing's own figure heights and scale labels stay in feet and inches; the Draw canvas on a sheet follows your units.
- **Light and dark themes:** the day-night button next to the logo. Dark is a neutral charcoal with a slight cool cast rather than pure black. Colors follow a Stabila-style palette: yellow, black, red, white and laser green. DIM follows the system setting until you pick one.
- **Notes:** a note's text sits apart from its tip, joined by a leader with an arrowhead. Drag the text (Edit or Note tool) to move it away from what it points at; drag the tip to repoint it. Rotated text keeps its arrow.

## Shop drawing

Sheets ready to send for approval: the drawing, a title block, your logo and a scale bar.

- **Sheets:** tabs above the sheet, named by sheet number. **+** adds a sheet that keeps the current paper, drawing source and project details and takes the next number (SD-1, SD-2…); **Duplicate** copies everything on the sheet too. Delete or reorder sheets under **Sheet**; Page Up / Page Down switch. Each sheet has its own paper, drawing, title block and items. **Export** makes one PDF with a page per sheet, each at its own size, or just the open sheet. Layout's **Open as shop drawing** goes to the sheet that already shows that job.
- **Guides:** **+ Vertical** and **+ Horizontal** under **Guides** add cyan lines that never print. Drag one with Select to move it (the selected guide shows its distance from the sheet edge; Shift moves in whole 1/8"), drag it off the sheet or press Delete to remove it. Text, shapes and images snap to guides as you move them; Alt places freely. New sheets keep the guides, so every sheet lines up.
- **Hand tool** (`H`): slides the drawing in its frame, for Draw canvases and Layout jobs alike; **Center drawing** puts it back.

- **Sheet:** Letter (8.5 × 11), Tabloid (11 × 17, the default), Arch C (18 × 24) or Arch D (24 × 36), landscape or portrait. A thin black border runs around the sheet.
- **Drawing:** the Draw canvas with its shapes and measurements (the whole page, or framed around the measurements), or any Layout job (mural, privacy film, distraction markers; tick which film rows, glass runs or elevations go on each sheet, and DIM arranges them to draw as large as fits). Fit it to the frame or pick a scale such as 1/4" = 1'-0"; a blank canvas's grid can be shown or hidden; the hand tool (`H`) slides it in its frame. Layout's **Open as shop drawing** button jumps here with that job.
- **Title block:** client name, project name, project location, date, sheet number and drawing title, plus your **company logo** (any image; DIM remembers it in this browser for the next job). The **scale bar** sits in the bottom right and can be turned off.
- **Text and shapes:** text boxes (font, size, bold, italic, alignment, color), rectangles, ellipses, lines and arrows, with outline and fill colors, line width and dashes. Each color row shows none, white, black, red, green and pink, then a **custom** tile: it opens a panel of color and gray swatches, with a **Wheel** view (your system color picker and a hex field). Fonts are Sans (Helvetica), Serif (Times) and Mono (Courier), the three built into every PDF, so the sheet and the PDF match. Click to drop one, or drag to size it; Shift keeps lines straight; drag the corner handles to resize; Delete removes; arrow keys nudge.
- **Layer order:** **Arrange** in the left panel sends the selected item to the back, backward, forward or to the front (Cmd+Shift+[, Cmd+[, Cmd+], Cmd+Shift+]; Ctrl on Windows). The On sheet list runs front to back.
- **People for scale:** the Person tool (`P`) drops a man (5'-10") or woman (5'-5") with their feet where you click. They stay true to the drawing's scale; change the height or swap the person in the left panel.
- **Export PDF:** a true-size PDF. The drawing prints at up to 300 ppi; the title block, text and shapes are vector, so they stay sharp.

## Projects and exports

- **Save project (.dim)** (or Ctrl+S): one file with the drawing, scales, measurements and Layout settings (including a mural image). Send it to a coworker; they open it with the same Open button.
- **Autosave:** DIM keeps the current project in the browser, so a refresh or closed tab picks up where you left off. A private window may not keep it.
- **Marked-up PDF:** your measurements drawn on the original sheet (vector, on top of the architect's PDF), plus a list page with totals.
- **Marked-up image (JPG):** the drawing or photo with your measurements burned in, at full photo resolution, easy to text or email.
- **Copy list** and **CSV** (with category, value, unit and inches).

## Layout

Plain numbers are inches; `24'`, `2'-6"` and `3.2 m` work too. Roll widths: 48", 54", 60" and 61". **Printer margin** (default 6", both edges together) sets the printable width, so a 54" roll prints 48" wide; murals and film are laid out on the printable width, and media used is counted on the full roll.

**Right panel:** the top names what you're editing (the selected film row or Graphic elevation, or the whole Mural or Markers job) with its size. Below it, tabs hold its settings: Look, Frame and Doors for a film row; Graphics, Wall, Frame and Doors for an elevation; Bands, Spacing, Frame and Doors for Markers; Wall, Artwork and Roll for a mural. Settings for the whole job (roll, coverage, cutting, dimensions) fold away under **Whole job**, each showing its current values in one line. The bar at the top switches between **Settings**, **Totals** (results and quote) and **Export** (files and Shop drawing). Tips are hidden until you press the **(i)** button in the corner; DIM remembers your choice. Warnings and numbers worked out for you (printable width, where the glass starts, nesting) always show.

**Dimensions:** Graphic, Film and Markers each have a **Dimensions** section under Whole job: icon buttons (hover for the name) switch each dimension on the preview and the shop drawing. Graphic: size, from the glass or wall edges, bottom, top and center above the floor. Film: film size (the strip sizes plus the film's overall width or height, so nothing repeats), **where the feather starts and stops** (a dashed line and a tag such as "Solid 36"" at each height; above the floor on a built-out row), and the band. Markers: band heights, top of marks above the floor, spacing between marks (now on plain runs too) and one mark's size. Dimension labels adapt to what's under them: plain text in whichever ink reads there, and a white box only over something dark, colored or busy (brick, a black frame, a mural). The shop drawing is white paper, so there the box shows only where the drawing itself is dark or colored. Butt joints between panes draw as a faint line, lighter than a mullion.

**Selecting several:** Shift+click adds or removes items in Graphic (on the drawing or their cards) and in Shop drawing (on the sheet or in the On sheet list). Drag one to move them all; Delete removes them all. Click an item that is already selected to make it the **key** item.

**Align (Graphic):** with graphics selected, pick what to align to, **Wall** (or **Glass**: the pane each graphic sits on), **Selection** (the box around the selected graphics) or **Key graphic** (the others line up to it and it stays put), then align left, center, right, top, middle or bottom.

**PDFs as artwork:** Graphic uploads and the Mural image take a PDF as well as an image. DIM uses its first page: a graphic keeps its transparent areas, and a mural image is drawn at as many pixels as the browser allows (check the image resolution under Totals).

**Mural image placement:** set **Fit** to **Place by hand**, or drag a filled or fitted image on the preview. Drag the image to move it and drag a corner to scale it (it keeps its shape), or type its width and its distance from the wall's left and top (negative goes past the edge). **Center**, **Fill wall** and **Fit inside** reset it.

- **Mural:** wall width and height (or a rectangle or length from Draw), bleed on each edge (default 1"), overlap between panels (default 1"), drops or rows, and all panels equal (the default) or full rolls with a trimmed last panel. **Drag a seam** on the preview to move it off a face or logo; later seams slide with it and the last panel takes up the difference. Fill with a solid color, a gradient or an image (fill, fit, stretch or a repeating pattern). Exports **panels as a true-size PDF** (one page per panel, with optional labels and seam marks in the bleed), a zip of PNG tiles, a panel map, a panel list and a CSV.
- **Privacy film:** glass panes (width, height, quantity) with a bleed on each edge, laid out as drops or rows, whichever uses less film, with **all strips equal** (the default) or full rolls and a trimmed last strip. The selected pane's strips show under the big number, e.g. **(3) drops @ 43.625"**, and every strip is dimensioned on the preview. **Add from Draw** turns rectangles and lengths (tagged Privacy film, or untagged) into panes. The film can be a printed gradient, **frost** (shown with the slightest warm tint, Lab 90 / −1 / +3), **feathered frost** (solid at one height, fully clear at another; fades up or down), or a **dual feather** (a frost band fading out above and below, or a clear band with frost fading in). Heights are from the bottom of the glass. Put a **person behind the glass** (man, woman or both) to show how much the film hides. Totals **glass area in sq ft** by default, or **linear feet of glass** (horizontal width × quantity; set with **Measure glass by**), plus media used, media area, seams and yield; the quote can charge by glass area, linear feet or media used. **Print file (PDF)** has one true-size page per strip with bleed: a printed gradient runs bottom to top across the whole pane, and frost looks print as grayscale (black is solid frost, white is clear) to map to white ink or a frost layer in the RIP. Strip labels (pane, drop or row number, size, how many to print) and glass-edge marks go in the bleed. **Bands:** under **Coverage**, switch **Film covers** from the whole glass to **A band**, then set the band height and its bottom edge above the floor (a 48" band from 24" to 72", say). One band runs the length of every row and is cut for each pane of glass, clipped where a door rail or sill gets in the way. A band's top and bottom edges get no bleed unless they reach the edge of the glass, so a 48" band prints as one row on a roll that prints 48". Plain panes are placed by **Sill height**. **Build out a wall:** select a row and use **+ Pane** and **+ Door** (or type `24, 24 | 36 Door | 48`) to give it a frame, mullions, butt joints and doors, the same builder Markers uses. Film is then cut for each pane's visible glass, door glass included (inside its stiles and rails), the preview draws the elevation with doors and hardware, and frost heights and gradients are set out from the floor so they line up across doors and sidelites. Frame, door and hardware settings are under **Frame**; each built-out row's H is its frame height. **Each row keeps its own Look and Frame:** the right panel edits the selected row (its name shows at the top of each section), a new row starts with the selected row's settings, and **Use on all rows** copies them to every row.
- **Distraction markers** (glass safety markings): glass runs, band heights (bottom edge AFF, above finished floor, e.g. `30, 60`), band height and pattern (squares, dots, vertical ticks, a solid line, or **your own graphics**: upload PNG or SVG files, labeled A, B, C…, and use the same one on every marker, each in turn, or your own sequence). In a sequence, capitals are your graphics and lowercase `q`, `b`, `o`, `d` and `l` are a square, a dark square, a dot, a dark dot and a vertical tick, so `A, l, l, l` is your logo followed by three ticks and `q, b` alternates light and dark squares. Or click the mark buttons under a sequence to add marks in order (⌫ removes the last); a preview shows the marks as they'll repeat.
  - **Own pattern on each band:** give each band its own sequence, e.g. `q, b` on the 60" band and plain squares on the 30" band. Marks line up from band to band.
  - **Start pattern:** centered on the run, from the left edge or from the right edge. The sequence counts from that end.
  - **Gap measured:** as clear space between marks, or **on center (O.C.)**, center to center, the way specs often call it (2" squares at 9 1/2" O.C. leave 7 1/2" clear).
  - **Spacing on panes:** *Minimum gap* treats the gap as a floor and spreads each pane's marks to fill its glass, so the gap you get can be larger. *Exact gap* keeps the gap you set, for when a client spec calls for it, and leaves the extra space at the glass edges: on the far edge when starting from left or right, split evenly when centered. Runs without panes always use the exact gap.
  - **Panes:** build the selected run's glass left to right with **+ Pane** and **+ Door**. Each pane has a width and a type (Glass, Door, or Fill rest, which takes whatever the run's length leaves, shared between several); click the line between two panes to switch a butt joint and a mullion. Doors pick their style and hinge side. **Run length** sets how the length and panes relate:
    - **Subtractive: fixed length** (new runs): type the wall or opening length, and **+ Pane** adds Fill rest panes that share what the doors, sized panes, jambs and mullions leave. Type a width into a Fill rest pane to fix it. The run warns when the panes come up short or run over.
    - **Additive: grows with panes:** each pane and door adds to the run; the first pane takes the run's length less the jambs. Switching to additive fixes each Fill rest pane at its current width.
    - **Type instead** shows the same panes as text, e.g. `34.5, 34.5 | 36 Door | 8`: commas are butt joints, bars are mullions, a word after a size names the pane, `3@48` is three 48" panes, and `*` fills the rest, so `*, * | 36 Door` on a 120" run works out the glass. Pane sizes are visible glass; a door's size is its opening. Without a `*`, the run's length comes from the panes and frame. Marks sit in each pane's glass, at least half a gap in from each edge, so none land on a seam, mullion or door stile; the sequence carries on across seams and starts again after each mullion. The selected run lists each pane size's marks, spacing and distance from the glass edges.
  - **Frame:** frame height, a curb or knee wall under the frame, jamb, mullion, head and sill sightlines (the frame's visible face), butt-joint width (3/8" by default) and color (black, dark bronze or clear anodized). The glass starts at curb plus sill.
  - **Doors:** add one with **+ Door** (or put `Door` in a pane's name). Doors run to the floor, with narrow (2 1/8"), medium (3 1/2") or wide (5") stiles, or all glass with no stiles (each door can override the default in the pane builder), top and bottom rails you set (3 1/2" and 10" by default), and hinges left or right. Hardware is a pull (with its length), push bar or exit device (panic); its height is measured to the top, AFF. A pull sits on the latch stile, or on the glass of an all-glass door. The swing can be shown as dashed lines meeting at the hinge side.
  - **Warnings:** a run flags bands that fall below or above the glass (on a curb, sill or door rail), marks within 1" of door hardware, and Fill panes that don't fit. Those marks are outlined red on the preview.
  - The preview draws the curb, frame, seams, doors, hardware, pane names, opening widths, overall width, where the glass starts, and the spacing in the first pane.
- **Quote** (each job): price and install rate per sq ft or LF, setup, minimum, rush, and what to charge on. Copy the quote into an email or PressWise. Prices are examples until you change them; DIM remembers yours in the browser.

**Privacy:** files open on your own device and are never uploaded. Autosave stays in this browser only.

**Accuracy:** always check the scale by measuring a dimension that's printed on the sheet. Values are shown to the nearest 1/16".

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The whole app: page, styles and script |
| `vendor/pdfjs/` | Mozilla pdf.js 3.11.174, which draws the PDFs (Apache-2.0, license included) |
| `vendor/pdf-lib/` | pdf-lib 1.17.1, which writes the marked-up and panel PDFs (MIT, license included) |
| `favicon.svg` | Tab icon |
| `apple-touch-icon.png`, `icon-192.png`, `icon-512.png` | App icons for Add to Dock / Home Screen and installed web apps |
| `manifest.webmanifest` | Web app name, colors and icons for installing |
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
