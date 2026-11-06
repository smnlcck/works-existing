# works-existing

A replica of the current [simonalcock.ie](https://simonalcock.ie) homepage Work section, rebuilt as a baseline for the section-by-section homepage redesign. Other Works variants will be compared against it.

Measured from the live site at 1440 × 900 and 1024 × 900:

- Grey full-width row, 10/12 centred column, 50/60 "Work" heading (hero-existing type styles)
- White card with a 30px radius and 24px top and bottom padding
- 21 tiles in a gutterless grid: 3 columns above 1024px, 2 columns from 641–1024px, 1 column below
- Every tile is 5:4, image `object-fit: cover`
- Hover: white 85% overlay fades in (0.25s), title then categories slide up from below (theme easing)
- Tiles 13–21 rise 30px and fade in on scroll, as the live site's second and third grids do

Changes from the live site:

- The overlay also shows on keyboard focus, with a visible focus ring
- On touch screens (no hover) the title and categories sit permanently along the bottom of each tile
- The three separate WordPress grids are merged into one list
- All motion is behind `prefers-reduced-motion`

Open `index.html` in a browser to view it. Images are copied from simonalcock.ie at 960px wide into `images/`.

## Fonts

Eudoxus Sans Medium is a licensed font, so it is not in this repo. The page loads it from simonalcock.ie. Browsers only allow that if simonalcock.ie sends an `Access-Control-Allow-Origin` header for its font files; without it, the text falls back to Helvetica.
