# Pixel Drift Arcade: A Browser Game Hub for an Indie Studio

**Category:** Web Development
**Project Type:** Responsive multi-section marketing and arcade website (static front end)
**Platform / Medium:** Web browser, desktop and mobile
**Deliverable Type:** Static site folder (HTML, CSS, JS) plus README

---

## Context

Pixel Drift Studio is a small independent team of three developers and one artist who have spent about two years building short, replayable browser games as a side project. The studio now wants one clean public home that introduces the team, displays its catalogue of games in a tidy grid, and lets a first time visitor play a simple game inside the page within seconds of arriving. The studio has a name and a loose retro pixel art mood, but no real website, no fixed colour palette, and no defined typography, so those choices are part of this build.

This milestone is a single static front end website. It is not a game engine, not a backend service, and not a content management system. The site must run entirely from static files served by any plain web server or opened from disk. There is no login, no database, no payment, and no server side code of any kind.

---

## Project Information

| Field | Details |
|---|---|
| Project Type | Multi-section static website with one embedded mini-game |
| Client / Brand | Pixel Drift Studio (fictional indie game studio) |
| Platform / Medium | Web browser, responsive from 320 pixels wide and up |
| Deliverable Type | Static site folder plus README.md |
| Primary Goal | A fast, responsive arcade hub that showcases the catalogue and lets visitors play one game in the page |

---

## Main Goal

The single most important outcome is a working, responsive, static website that loads the studio brand, lists every game from the provided dataset in a filterable grid, and runs one fully playable keyboard controlled mini-game directly inside the page with a local high score that survives a page refresh. The site must be built only with HTML, CSS, and plain JavaScript, and must open and run without any build step, paid plugin, or internet connection.

1. A branded landing section that introduces Pixel Drift Studio.
2. A filterable catalogue grid built from the provided `games.json` dataset.
3. One embedded, playable canvas mini-game with a saved high score.

---

## About Pixel Drift Studio

Pixel Drift Studio is a four person independent team, three developers and one artist, that has been making tiny browser games for roughly two years. No website exists yet, no logo file is provided, no colour palette is fixed, and no typography is chosen. The brand identity beyond the name and the retro arcade mood is open for the freelancer to define within the rules listed in this brief.

**Brand tone:** playful, retro arcade, energetic, readable, fast to load.
**Brand line:** `Small games. Big drift.`

---

## Requirements

The freelancer will build a single responsive website made of stacked sections on one page, plus one embedded canvas mini-game, using only HTML, CSS, and vanilla JavaScript.

### Core Functionality

1. The site is a single HTML page made of stacked sections, navigated by a sticky top bar.
2. The sticky navigation bar links to four sections by name: Home, Games, Play, and Contact.
3. Clicking a navigation link scrolls smoothly to the matching section.
4. The site is responsive and remains usable from a viewport width of 320 pixels up to 1920 pixels.
5. The site runs from static files with no backend, no database, and no build step.
6. Opening `index.html` in a modern browser shows the full site with no console errors.

### Home Section

- A hero area shows the studio name Pixel Drift Studio, the brand line `Small games. Big drift.`, and one call to action button labelled Play Now.
- The Play Now button scrolls smoothly to the Play section.
- The hero area includes a short studio summary of two to three sentences drawn from the context above.

### Games Catalogue Section

- The catalogue reads its content at runtime from the file `data/games.json` provided in this task.
- Each game in the dataset renders as a card showing its title, genre, release year, a one line description, and a thumbnail colour block built from the `color` field.
- A filter control lets the visitor filter cards by genre. The genre options are built automatically from the values present in the dataset.
- Selecting a genre shows only cards of that genre. Selecting the All option shows every card.
- The card count visible on screen updates to match the active filter.
- The dataset holds at least ten games and the grid shows all of them when the All filter is active.

### Play Section (Embedded Mini-Game)

- The Play section embeds one playable mini-game drawn on an HTML5 canvas element.
- The mini-game is a single avatar that drifts left and right across the bottom of the canvas, controlled by the left and right arrow keys, catching falling blocks that spawn from the top.
- Catching a falling block adds one point to the current score. A missed block that reaches the bottom edge removes one life.
- The player starts with three lives. When lives reach zero the game shows a Game Over message and a Restart button.
- The current score and remaining lives are shown on screen during play at all times.
- The highest score reached is saved to the browser using local storage under the key `pixelDriftHighScore` and is shown on screen.
- The saved high score persists after a full page refresh.
- A Restart button resets the score and lives to the starting values and begins a new round without reloading the page.

### Contact Section

- The Contact section shows a static contact block with a studio email placeholder reading `hello@pixeldrift.studio` and a one line invitation to get in touch.
- The Contact section includes a simple form with a name field, an email field, and a message field, plus a Send button.
- The form validates that all three fields are filled before it accepts a submission. An empty field shows an inline message asking for the missing value.
- On a valid submission the form clears its fields and shows an on screen thank you message. The form does not send data anywhere and no backend is involved.

---

## Visual and Technical Specs

### Dimensions and Layout

- **Canvas game size:** `480 x 360 px` drawing surface, scaled responsively to fit its container.
- **Maximum content width:** `1200 px`, centred on the page.
- **Minimum supported viewport:** `320 px` wide.
- **Card grid:** at least three columns on screens `1024 px` and wider, at least two columns between `640 px` and `1023 px`, and one column below `640 px`.

### Typography

| Usage | Font | Notes |
|---|---|---|
| Headings | A geometric or pixel style web safe or open licensed font | Bold weight, used for section titles and the studio name |
| Body | A clean sans serif such as Arial, Helvetica, or an open licensed equivalent | Regular weight, minimum 16 pixel base size |
| Score and game text | A monospace font such as Courier New or an open licensed equivalent | Used inside the game for score and lives |

**Not allowed:** decorative script fonts, handwriting fonts, and fonts that require a paid licence.

### Colours

The exact palette is open for the freelancer to choose, within these rules.

**Colour rules:**
1. The palette uses at most five colours plus black and white.
2. Body text keeps a contrast ratio of at least 4.5 to 1 against its background.
3. The chosen accent colour is reused for buttons, active navigation links, and active filter states so the look stays consistent.
4. Each game card thumbnail block uses the `color` hex value from that game record in the dataset.

---

## Technical Requirements

- **Framework:** none. Plain HTML, CSS, and vanilla JavaScript only.
- **Language:** HTML5, CSS3, and standard JavaScript that runs in current browsers.
- **Platform / Target:** responsive web, working from 320 pixels wide and up.
- **Storage:** browser local storage for the high score only.
- **Data source:** the provided static `data/games.json` file, loaded at runtime.
- **Browser support:** the latest stable versions of Chrome, Edge, Firefox, and Safari.
- **Code quality:** clean, commented, and organised into sensible folders.

### Allowed Tech Stack
1. HTML5, CSS3, vanilla JavaScript.
2. CSS Flexbox or CSS Grid for layout.
3. The HTML5 Canvas API for the mini-game.

### Not Allowed
- Front end frameworks or libraries such as React, Vue, Angular, jQuery, or Bootstrap.
- Backend servers, databases, or authentication.
- Paid plugins, paid fonts, or paid assets.
- Build tools that require a compile step before the site runs.

---

## Design Direction

**Do:**
- Lean into a retro arcade look with bold blocks of colour and crisp edges.
- Keep navigation obvious and the Play Now path short.
- Keep load fast by using only local assets and a small amount of code.

**Do not:**
- Use heavy background videos or large unoptimised images.
- Add gradients, glows, or drop shadows so dense that text becomes hard to read.
- Copy the look, logo, characters, or names of any real game company or real game.

---

## Reference Materials

| Asset | File |
|---|---|
| Game catalogue dataset | `data/games.json` |
| Layout reference mockup | `reference_image.png` |

**How to use these references:** The `games.json` file is the only source of truth for the catalogue content and must be read at runtime rather than hard coded into the HTML. The `reference_image.png` shows the intended section order and rough block layout. Match the section order and the general arrangement. Exact spacing, colour, and font choices are open within the rules in this brief. Where a reference detail conflicts with a written requirement, the written requirement wins.

---

## Dataset Specification

The catalogue is driven by `data/games.json`, a single JSON array of game records. Each record has the fields below. The seller must not rename these fields.

| Field | Type | Meaning |
|---|---|---|
| `id` | number | Unique id for the game |
| `title` | text | Game title shown on the card |
| `genre` | text | Genre used by the filter control |
| `year` | number | Release year shown on the card |
| `description` | text | One line description shown on the card |
| `color` | text | Hex colour string used for the card thumbnail block |

The provided dataset holds at least ten records and at least four distinct genres. All catalogue content on the site comes from this file.

---

## Deliverables

| # | Item | Format | Notes |
|---|---|---|---|
| 1 | `index.html` | `.html` | Single page holding all four sections |
| 2 | Stylesheet | `.css` | All site styling, placed in a `css` folder |
| 3 | Site script | `.js` | Navigation, catalogue rendering, filter, and form logic, in a `js` folder |
| 4 | Game script | `.js` | The canvas mini-game logic, in the `js` folder |
| 5 | `games.json` | `.json` | The provided dataset, placed in a `data` folder and read at runtime |
| 6 | Any images or icons used | `.png` or `.svg` | Local only, in an `assets` folder |
| 7 | README.md | `.md` | Setup and run instructions |

### File Naming Convention

All delivered files use lowercase kebab-case names with no spaces. Folder names are lowercase.

### Folder Structure

```
pixel-drift-arcade/
  index.html
  css/
    styles.css
  js/
    main.js
    game.js
  data/
    games.json
  assets/
    [local images or icons]
  README.md
```

---

## Scope Boundaries

### DO
- Build a complete responsive single page site with the four sections described.
- Read all catalogue content from the provided dataset at runtime.
- Build one playable canvas mini-game with score, lives, restart, and a saved high score.
- Use free, open licensed, or self made placeholder assets where images are needed.

### DO NOT
- Build any backend, database, account system, or payment.
- Add a second page or a routing system. The site is one page with stacked sections.
- Use any front end framework or third party UI library.
- Copy real brand names, logos, characters, or artwork from any existing company or game.

---

## Tool Requirements

- **Required tools:** any plain text or code editor and a modern web browser.
- **Acceptable alternatives:** any editor of the freelancer choice.
- **Forbidden:** paid plugins, paid fonts, and paid stock assets.

---

## Quality Control Checklist

Before submitting, confirm all of the following.

1. [ ] `index.html` opens in a modern browser with no console errors.
2. [ ] The sticky navigation links scroll smoothly to Home, Games, Play, and Contact.
3. [ ] The catalogue grid renders every record from `data/games.json` when the All filter is active.
4. [ ] The genre filter shows only matching cards and the visible card count updates.
5. [ ] The mini-game responds to the left and right arrow keys.
6. [ ] Catching a block adds a point and a missed block removes a life.
7. [ ] Reaching zero lives shows Game Over and a working Restart button.
8. [ ] The high score is saved under `pixelDriftHighScore` and survives a page refresh.
9. [ ] The contact form blocks empty fields and shows a thank you message on a valid submit.
10. [ ] The layout holds together from 320 pixels up to 1920 pixels wide.
11. [ ] All file and folder names follow the lowercase kebab-case rule.
12. [ ] No paid asset, framework, or backend is used anywhere.

---

## Acceptance Checklist

The delivery is complete only if every item passes.

1. [ ] The site is one HTML page with four named sections navigated by a sticky bar.
2. [ ] All catalogue content is loaded at runtime from `data/games.json`.
3. [ ] The grid shows at least ten game cards under the All filter.
4. [ ] The genre filter works and the visible count updates with the active filter.
5. [ ] The embedded mini-game is playable with arrow keys and tracks score and lives.
6. [ ] Lives start at three and Game Over appears at zero lives with a Restart button.
7. [ ] The high score persists after a page refresh through local storage.
8. [ ] The contact form validates three fields and clears on a valid submit.
9. [ ] The site is responsive from 320 pixels and up with the required column counts.
10. [ ] The delivered folder matches the required structure and a README explains how to run it.

---

## Evaluation Criteria

- Section order and the four named sections match this brief.
- Catalogue content is driven by the dataset and not hard coded.
- The genre filter is correct and the card count matches the filter.
- The mini-game scoring, lives, restart, and saved high score all behave as described.
- Responsive behaviour holds at 320, 640, 1024, and 1920 pixel widths.
- Contact form validation and reset behave as described.
- Code is clean, commented, and organised into the required folders.
- No real brand, logo, or copyrighted asset appears anywhere.

---

## Delivery Terms

- **Revisions included:** one round of minor revisions.
- **Allowed revision types:** colour adjustments, spacing changes, copy fixes, and small layout tweaks.
- **What does not count as a revision:** a full redesign, a new section, or any scope expansion beyond this brief.
- **Delivery method:** a single compressed folder of the static site that matches the required structure.

---

## Final Goal

Success looks like a small, fast, and cheerful arcade website that a first time visitor can open, scroll through to meet Pixel Drift Studio, browse a filterable shelf of the studio games, and within seconds play a simple block catching game whose best score is still waiting after the page reloads. The result feels like a real indie studio front door, built cleanly from static files, easy to host anywhere, and ready to grow as the studio adds more games.
