# Math Coaster

Build a roller coaster track from function pieces, connect them with no gaps, ride it, and use synthetic division to find where a polynomial track meets the ground.

**Live site:** <https://jontaylormed.github.io/math-coaster/>

**Source:** <https://github.com/jontaylormed/math-coaster>

**Site created by Claude and Jon Taylor.**

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

---

## What it does

| Section | What the student does |
|---|---|
| Intro | Reads the challenge: at least 4 function pieces, at least one hill, starting and ending at ground level (y = 0), with no gaps |
| Coaster Builder | Types each piece as an equation with its own domain (linear ramps, parabola hills, sine waves, cubics), sees whether each piece meets the next, then launches cars to ride the track |
| Sample Tracks | Loads or adds five ready-made tracks to study and change |
| Synthetic Division Explorer | Enters a polynomial and a value r, then works the division one step at a time: bring down, multiply, add |
| Remainder Theorem graph | Sees the polynomial's graph with p(r) marked, and picks a piece of the curve to copy into the builder as a track segment |

## Who it's for

Algebra II, usually grades 10–12.

Common Core State Standards for Mathematics:

| Standard | What it asks |
|---|---|
| HSF.IF.C.7b | Graph piecewise-defined functions |
| HSF.BF.B.3 | Identify the effect on a graph of replacing f(x) with f(x) + k, k·f(x), f(kx) or f(x + k) |
| HSA.APR.B.2 | Know and apply the Remainder Theorem: dividing p(x) by (x − a) leaves remainder p(a) |
| HSA.APR.B.3 | Identify zeros of polynomials from a factorization, and use them to sketch the graph |

## How it teaches

- **See it first.** Every equation becomes a piece of track right away, and a car rides it. The division explorer shows p(r) on the graph next to the remainder it matches.
- **Structure before numbers.** A track is a piecewise function. Students plan each piece's domain and where it starts and ends before they tune the numbers.
- **Check every claim.** The builder checks every join and says "continuous" or "discontinuous at x = …". The division result shows the remainder and p(r) side by side, so students see the Remainder Theorem hold.
- **No one feels remedial.** There are no scores or grades. Students build, test and fix.

## How the math was checked

- **Checks page:** [`checks.html`](https://jontaylormed.github.io/math-coaster/checks.html) runs 98 checks in the browser. All 98 pass. They cover:
  - every synthetic division sample: each step, the remainder against p(r) found by a separate method, and (x − r) × quotient + remainder rebuilt to equal p(x);
  - the intro's worked example and the roots it states;
  - every join in every sample track;
  - 16 equations through the equation reader;
  - keyboard use, contrast, labels;
  - a scan for outside requests and storage.
- **Fixed after checking:**
  - The equation reader rejected the intro's own hill example, `-(x-4)²+6`, as well as `2sin(x)` and `2(x+1)`. All three now work.
  - A sample was labeled "rational root test", but ½ isn't a possible rational root of 3x³ − 2x² + x − 4.
  - The labels under the division table called the constant column "x".
  - The graph note said every root "crosses" the x-axis. A double root only touches it.
  - The intro said the steeper the slope, the faster the car. The ride actually slows uphill and speeds up downhill.
  - "Connect smoothly" now says "connect with no gaps", which is what the app checks.
- **Known limits:**
  - Joins are checked within 0.02 in x and 0.05 in y, so a rounded endpoint such as 6.789 still counts.
  - Slopes aren't checked, so a corner where two pieces meet counts as connected.
  - The car's speed is a simple model, not real physics.
  - The equation reader understands sin, cos, tan, sqrt, abs, log or ln, pi and e.

## Accessibility

- **Keyboard:** everything works with the keyboard, and focus outlines are visible.
  - The tabs, sample tracks, division samples and buttons work with Tab and Enter.
  - The track-segment handles move with the arrow keys: 0.1 per press, or 1 with Shift.
  - The view can be set by typing in its boxes or with the zoom buttons, as well as by dragging.
- **Contrast:** text meets the WCAG 2.1 AA target of 4.5:1. Body text is 14:1, and hint text and graph numbers are 4.9:1 or better.
- **Screen readers:**
  - The track drawing is described in words, segment by segment.
  - The division graph is described by the note under it.
  - The ride status, division result and graph note are read aloud.
  - Every box is labeled.
- **Motion:** when the device asks for reduced motion, the animated intro picture and other animations stop. The coaster ride runs only when a student presses Launch.
- **Text size:** there is no separate setting; the page follows browser zoom.

## Privacy

No accounts, no tracking, no cookies and no stored data. The page makes no network requests: its typefaces are built into the file, and `checks.html` confirms nothing loads from outside.

## Running it

Open `index.html` in any modern browser.

`checks.html` reads the tool, so open it from the live site or any local web server, not as a file.

**Publishing:** GitHub Pages, deployed from the `main` branch at the repository root. There is no build step.

## License

[CC BY-NC-SA 4.0](LICENSE). Free to share and adapt for non-commercial use, with credit, under the same license.

The bundled typefaces keep their own licenses, and their license files are in [`fonts/`](fonts/):

| Typeface | Designer | License |
|---|---|---|
| Caveat | Impallari Type | [SIL Open Font License 1.1](fonts/OFL-caveat.txt) |
| Special Elite | Astigmatic | [Apache License 2.0](fonts/LICENSE-specialelite.txt) |
| Courier Prime | Alan Dague-Greene | [SIL Open Font License 1.1](fonts/OFL-courierprime.txt) |
