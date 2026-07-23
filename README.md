# Pro Cabinet Door & Material Calculator

A single-file web app for woodworkers building 5-piece (Shaker-style) cabinet doors. Enter your cabinet opening and joinery specs, and it instantly returns finished door sizes, a full cut list, hardware counts, material estimates, and a scaled visual layout — in either **imperial (inches/fractions)** or **metric (mm)**.

Everything lives in one `index.html` file. There is nothing to install and no internet connection required.

---

## Getting started

Just open `index.html` in any modern web browser (Chrome, Safari, Firefox, Edge) — double-click the file, or drag it into a browser window. It also works on a phone or tablet browser.

To keep it handy, bookmark the opened file or add it to your home screen.

---

## Quick start (60 seconds)

1. Tap a **preset** at the top of the input panel (e.g. *Wall pair*) to load a typical setup, or skip this and enter your own numbers.
2. Type your **Opening Width** and **Opening Height** (measured inside the cabinet frame).
3. Pick your **Cabinet Style** (Overlay, Inset, or Frameless) and **Number of Doors**.
4. Read the results on the right — they update **as you type**. No calculate button to press.
5. Hit **Copy Cut List** to send the numbers to your phone, or **Print** for a shop copy.
6. Hit **Reset** to zero out every dimension field and start a new door from scratch.

---

## Choosing units

Use the **Imperial / Metric** toggle in the top-right corner.

- **Imperial** shows and accepts fractions (see below). Results round to the nearest 1/16".
- **Metric** shows millimeters. Results round to the nearest 0.5 mm.

Switching units re-displays every field and result in the new unit without losing precision — the math always runs internally in inches, so you can flip back and forth freely.

Every result line also shows the *other* unit as small gray text underneath, so you always see both at a glance.

---

## Typing fractions (imperial mode)

Input boxes accept fractions the way you'd write them on a board:

| Type this | Means |
|-----------|-------|
| `1 3/4`   | one and three-quarters |
| `3/8`     | three-eighths |
| `2 1/4`   | two and one-quarter |
| `1-3/4`   | one and three-quarters (dash also works) |
| `.5`      | one-half |
| `2.25`    | decimals are fine too |

When you click or tab out of a field, your entry is tidied into a clean, reduced fraction — type `0.5` and it becomes `1/2`; type `1.75` and it becomes `1 3/4`.

**Steppers:** every dimension field has **−** and **+** buttons that nudge the value by 1/16" (or 1/32" for the fine Gap and Expansion fields). You can also press the **↑ / ↓ arrow keys** while a field is selected. In metric mode the steppers move by 0.5 mm.

If you type something that can't be read, the field outlines in red and a warning appears — just correct it.

---

## The input fields explained

### 1. Opening & Style

- **Cabinet Style** — *Overlay* doors sit on top of the frame; *Inset* doors sit flush inside the opening; *Frameless (Euro/32mm)* doors mount straight to the cabinet box, no face frame. (Picking Inset or Frameless hides the Overlay field, and the Opening/Gap labels relabel to Cabinet Box Width/Height and Reveal Gap for Frameless.)
- **Opening Width / Height** (or **Cabinet Box Width / Height** in Frameless mode) — the **inside clear opening** of the face frame for Overlay/Inset, or the **outer box dimensions** for Frameless. Measure at both top & bottom (and both sides) and use the **smaller** reading if the frame is out of square.
- **Overlay (per side)** — how far each door edge covers the frame. ~1/2" is common for partial overlay.
- **Gap / Clearance** (or **Reveal Gap** in Frameless mode) — the center gap between a pair of doors, the reveal around inset doors, or the reveal between a frameless door and the box edge / between stacked drawer fronts. Typically 1/16"–1/8".

### 2. Door Configuration

- **Number of Doors** — one door, or a matched pair opening from the center.
- **Panel Layout** — a *Single Panel*, or a *Vertical Split Panel* (adds a center mullion and two panels).

### 3. Shaker Joinery Specs

- **Stile / Rail Width** — the width of the door's frame boards (e.g. 2 1/4").
- **Groove Depth** — how deep the panel groove is cut into rails and stiles.
- **Expansion Gap** — small clearance so the panel can swell with humidity without cracking the frame. Keep it small (~1/16").
- **Panel Material** — pick the panel stock thickness: 1/4" plywood/MDF for a standard flat (floating) panel, or 3/4" for a raised panel (raised profiles need the extra depth to shape — 1/2" usually isn't thick enough to raise).

### 4. Drawer Fronts

- **Number of Drawer Fronts** — set to *None* to skip, or 1–6 to size a stack of flat slab drawer fronts spanning the same opening width as the doors above.
- **Drawer Bank Opening Height** — the combined opening height for the whole drawer stack, measured the same way as the door opening. The app applies your Cabinet Style's overlay/inset/frameless formula to it, then splits the result evenly across the fronts with a reveal gap between each.

---

## Reading the results

- **Finished Door Dimensions** — the outside size of each finished door, plus how many doors are in the run.
- **Hardware Needed** — hinge count (auto-scales with door height: 2, 3, or 4 per door), pulls/handles, and drawer slides (1 pair per drawer front, if any are set).
- **Shaker Cut List (per door)** — sizes for the 2 stiles, rails, optional center mullion, and panel(s). These are your actual cut dimensions.
- **Drawer Fronts** — shown only when Number of Drawer Fronts > 0: each slab front's finished width × height.
- **Material Estimate (total job)** — linear feet of frame stock (with 15% waste added), board feet of 4/4 lumber, panel material area, drawer front area (if any), and a **sheet goods** count — how many 4×8 ft sheets of plywood/MDF to buy, based on total panel + drawer front area with 15% waste (area-based estimate, not a cut-layout/nesting plan).
- **Visual Scale Layout** — a simple scaled drawing of the door(s) and panel arrangement.

---

## Presets

Three one-tap starting points:

- **Base door** — a single 15" × 24" overlay door.
- **Wall pair** — two 30" × 30" overlay doors.
- **Tall pantry** — a tall 24" × 84" split-panel pair.

Load a preset, then adjust any field to fit your project.

---

## Copy, Print & Reset

- **Copy Cut List** copies a clean, plain-text version of the cut list and materials (with both units shown) to your clipboard — paste it into a text, email, or notes app.
- **Print** opens your browser's print dialog with a light, ink-friendly layout that drops the dark background and on-screen controls.
- **Reset** zeroes out every dimension field (opening/box size, overlay, gap, stile width, groove, expansion, drawer height) and sets Drawer Fronts back to None — a clean slate for starting a new door. It won't touch your Cabinet Style, Door Count, Panel Layout, or Panel Material selections.

---

## Reference guide

Scroll to the bottom of the app and expand **Cabinet door guide & reference** for:

- a labeled diagram of a 5-piece door's anatomy,
- the four door styles (inset, lipped, partial overlay, full overlay) and how each fits the opening,
- how to measure the opening,
- all the formulas plus a worked example,
- the four common corner joint profiles (90°/Shaker, bevel, ogee, radius),
- how frameless (Euro/32mm) cabinet sizing differs from framed, and
- how drawer front sizing works.

---

## How the math works (formulas)

**Finished door size**

```
Overlay, single:    Door W = Opening W + (2 × Overlay)
                    Door H = Opening H + (2 × Overlay)
Overlay, pair:      Door W = [(Opening W + 2×Overlay) − Center Gap] ÷ 2
Inset, single:      Door W = Opening W − (2 × Clearance)
Frameless, single:  Door W = Box W − (2 × Reveal)   (same formula as Inset, applied to the box)
```

**Drawer front size (per stack)**

```
Bank W/H = same style formula as above, applied to the drawer opening
Each front H = (Bank H − (Count − 1) × Reveal) ÷ Count
Front W = Bank W (spans the full opening)
```

**Cut list (per door)**

```
Stile length = finished Door Height
Rail length  = Door W − (2 × Stile Width) + (2 × Groove Depth)
Panel width  = Door W − (2 × Stile Width) + (2 × Groove Depth) − (2 × Expansion Gap)
Panel height uses the same method with door height and rail width.
```

Unit conversion uses **1 inch = 25.4 mm**.

---

## Tips & troubleshooting

- **Results won't appear / show a warning box.** Check that opening width and height are positive, and that your stile width isn't wider than the door itself. The warning banner names the specific problem.
- **A field is outlined red.** The text can't be parsed as a number or fraction — retype it (e.g. `3/8`, not `3\8`).
- **Numbers look off after switching units.** They aren't — the display just rounds to the nearest 1/16" or 0.5 mm. The underlying value is preserved.
- **Always cut a test piece first.** These are calculated targets; verify against your actual cabinet before cutting a full batch.

---

## Technical notes

- **Single file, no dependencies.** Plain HTML, CSS, and JavaScript. No build step, no frameworks, no network calls.
- **Works offline.** Once the file is on your device, it runs with no connection.
- **Your data stays local.** Nothing is uploaded or saved anywhere; refreshing the page restores the original defaults (the in-app **Reset** button instead zeroes every field, for starting a new door without reloading).

---

## Disclaimer

This tool provides calculated estimates to assist planning. Always double-check critical dimensions and cut a test piece before committing expensive stock. You are responsible for verifying measurements for your specific cabinets and materials.
