# The Unsaid Collection

A universal, personal-message website. Suitable for appreciation, gratitude, friendship, farewell, memories, or words that were never said out loud.

## What's changed
- New pastel editorial look (cream, blush pink, light blue and navy) with an oversized serif headline.
- Neutral branding, landing-page text, letter-intro text and end-of-letter confirmation flow.
- Existing 30 *original personal messages*, unique recipient styles, and all randomized ticket codes **unchanged**.
- Music toggle, ticket validation, reading transitions and local one-time-read behavior kept intact.

## Run locally
Open `index.html` in a browser. For best testing, use a local static server, e.g. `python -m http.server 8000`, and visit `http://localhost:8000/`.

## Publish with GitHub Pages
1. Upload the **contents of this folder** to the root of a GitHub repository.
2. Go to **Settings > Pages**.
3. Choose **Deploy from a branch**, branch `main` and folder `/ (root)`, then save.

## Edit your letters
Open `js/messages.js`. Each ticket number is a key and its associated object contains `name`, `paragraphs`, `greeting` and other letter metadata.

To create a brand-new collection, replace the current entries and choose new non-guessable codes. Update recipient details without changing the surrounding JavaScript structure. The visible site identity is not tied to KKN anymore; any KKN mentions in the current letter bodies remain exactly as authored.

To change global wording or styling: `index.html`, `message.html` and `css/unsaid-redesign.css`.

## Important privacy limitation
This is a *static client-side* website. Ticket codes and letters are stored in JavaScript sent to visitors' browsers, and one-time-read state exists **only in a visitor's local browser**. It does not provide server-side access control or prevent screenshots or access by someone who inspects the source. Do not use it to share sensitive private information. Existing privacy deterrents are only visual / browser-level.

## Included assets
- `assets/audio/titik-nadir-soft.mp3`: existing background audio (unchanged)
- `assets/branding/`: original UNSENT brand assets and favicon (unchanged)

## Update: animated, personalized color journey (31 October 2026)

- The first screen has restrained floating paper, star glints and slow gradient drift.
- After a valid ticket is entered, the success overlay adopts that recipient’s actual color palette.
- The personalized introduction (second screen) now borrows colors directly from the matching unique letter (third screen); opening the envelope blends into the saturated letter-world gradient.
- All 30 ticket entries, letter contents, audio controls, once-read storage behavior and GitHub Pages static hosting are retained.
- Animations respect `prefers-reduced-motion` for users who request less movement.
