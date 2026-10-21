# Material Stories

An original, fictional interiors portfolio with an interactive material studio. Architectural SVG illustrations, warm paper tones, oversized serif typography, and a deliberate editorial grid give three imagined spaces their own visual story.

## Explore

- Three fictional projects: The Courtyard House, An Artist’s Atelier, and The Reading Room.
- Three coordinated finish palettes update each live interior illustration.
- Accessible native range input reveals the original shell against the furnished composition; keyboard arrow keys work too.
- Save one composition per project, add notes, refine or remove it, and clear your board with confirmation.
- Download a plain-text design brief containing the selected spaces, finish palettes, and notes.
- Local persistence with validated storage data and an in-memory fallback when storage is unavailable.
- Responsive layouts, semantic controls, visible keyboard focus, and reduced-motion support.

## Run locally

Requires Node.js 22 or newer. There are no install steps or external dependencies.

```sh
node scripts/serve.mjs
# Open http://127.0.0.1:4173
node --test
node scripts/build.mjs
```

Equivalent `npm run dev`, `npm test`, and `npm run build` commands are supplied if npm is installed. The lockfile records the dependency-free package. Deploy `dist/` on any static host; relative asset URLs support subdirectories.

## Architecture

`model.js` contains the original project data, palette data, storage validation, immutable board updates, brief generation, and SVG illustration renderer. `app.js` owns DOM interactions and browser-local state. `style.css` defines the editorial responsive design. The build script copies the four application files into `dist/`. Tests use Node’s built-in test runner and cover malformed stored data, duplicate/oversized records, replacement semantics, exported briefs, and illustration states.

## Privacy and limitations

This is a portfolio demonstration, not an operating interior-design practice. All spaces, names, and details are fictional. Illustrations are original SVG artwork, not photographs or documentation of client engagements. Material colors are approximate screen representations. No personal information is sent anywhere; notes and compositions stay in this browser. Clearing site data removes saved boards, and private browsing or restricted storage may limit persistence. The brief is a text file, not a construction specification. No analytics, accounts, APIs, fonts, or remote assets are used.

No open-source license has been selected. This repository intentionally does not include a LICENSE file.

## Visual review

Screenshots and actual browser-review results are recorded by the publishing workflow after implementation. No browser review is implied solely by the automated tests.


Detailed executed checks and verification limits: [QA record](QA.md).
