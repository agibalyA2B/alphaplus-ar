# Alpha+ pitch — Team 4

## Publish to GitHub Pages

Upload **the `pitch` folder** to the root of `agibalyA2B/alphaplus-ar`, leaving the existing viewer and model files untouched. The only runtime site file is `pitch/index.html`: CSS, JavaScript, React, Motion, GSAP and the original Number Ticker component are bundled inline. No build, npm install, API key or server is needed to publish.

Open the repository’s existing Pages URL and append `/pitch/`. Test from the Pages URL, not just an HTML email/file preview. The website has not been pushed or deployed for you.

Fonts load from Google Fonts; the optional 3D viewer loads its module from jsDelivr and your existing GLB/USDZ from your Pages root. The text and schematic remain usable if these fail. No video request is made until a film URL is added. Check the webinar network ahead of time. For an offline talk, open once online or self-host the fonts and model-viewer module.

## Swap in the film

Open `index.html` in a text/code editor. Search for `id="media-config"` near the bottom. This readable JSON block holds the media fields `film`, `heroFilm`, `captions`, `poster`, initially empty strings. Set them to relative file paths or public URLs, for example:

```js
{"film":"./assets/khalid-journey.mp4","heroFilm":"./assets/hero-loop.mp4","captions":"./assets/khalid-en.vtt","poster":"./assets/film-poster.jpg","aiGenerated":true}
```

Keep valid JSON punctuation and double quotes. Create `pitch/assets/` and upload the files there. Use an H.264 MP4 with AAC audio and a caption file in WebVTT format. The main film has native play/pause, seek and volume controls; it never auto-plays. The optional hero loop is muted and has no audio controls; it does not auto-play for reduced-motion users. It should be a short background crop of the main story, not required information.

**All AI-generated images or film must be labelled “AI-generated concept visualisation”.** The film configuration automatically shows that caption while `aiGenerated` is true. Set false only for genuinely non-AI footage and update its credit. Make any provided clip finish on the calm, happy commuter; the current closing is text-led because no film or image was supplied. No media has been generated for this package. HyperFrames was not needed for an unsupplied film.

## Edit copy, figures, names and links

- All narrative copy is ordinary readable HTML **before the inline script**. Search for a visible sentence to edit it. Preserve headings, IDs and accessibility labels.
- For every animated number update **both** `data-number="…"` and the visible text inside its span. Decimal precision uses `data-decimals="2"`. Update the adjacent source and unit too.
- Search for `[Member 1` through `[Member 5` and replace the five marked placeholders.
- Search for `FULL MODEL` in the financial details and closing. Replace the pending spans with a real `<a href="YOUR_PUBLISHED_MODEL_URL">Full model ↗</a>` only when you have that URL. Update the sources dialog too.
- Model v5 is in `pitch/assets/Alpha_Plus_model_v5.xlsx` and linked from the economics section, its details panel, the Sources dialog and the closing. The repo is public, so anyone with the link can download it.
- The comparison is qualitative draft material, not tested product performance. Verify exact comparator models, prices, lids and scheme details before removing caveats. Do not claim a paper-cup cost or carbon advantage.
- 802M is rounded **passenger ridership across public transport, shared mobility and taxis**, not vehicle trips, Metro-only use or unique people.
- Environmental claim: CHOICE/CIRAIG give about 40 to 50 uses for a stainless cup to break even on climate impact; Team 4 converts uses to a return rate with uses = 1 ÷ (1 − r), so about 97.5% returns. The page states the conversion as a Team 4 modelling assumption; the pilot measures actual impact.
- Closed-drink carriage: the fine schedule (Resolution No. 3 of 2026, Schedule 3) has no provision against carrying a closed non-alcoholic drink (Team 4 reading). Station food-and-drink permission stays a hard pilot gate.

## Present live (~10 minutes)

Click **Present**, then use **← / →** or **Page Up / Page Down** to move through chapters. **Esc** exits presenter mode (or closes an open dialog). The four service steps are scroll-paced rather than timed: scroll slowly through them, or simply stop and explain. The comparison reveals across each row when it comes into view. Its table scrolls sideways on phones; every row remains readable without animation.

Suggested pacing: morning problem + Khalid 1:30; hook and film 1:30; four steps 2:00; comparison 1:00; economics 1:30; staged recommendation 1:30; closing 1:00. Adjust the film to keep the total near ten minutes. The film is currently a visible slot, not a fake play button.

Use **Motion: off** to stop the ambient and looping hero motion. OS reduced motion also disables scroll animations and initial number count-ups. Native disclosures hold detail; Sources and CAD use keyboard-accessible dialogs. Focus rings are visible. No flashing or autoplay audio.

## Design provenance and licence

- Palette: **Ocean Five**, DESIGNJUNKEE, https://www.colourlovers.com/palette/1473 — CC-BY-NC-SA. Palette-derived work is for noncommercial educational use, with attribution and share-alike terms. Do not reuse this palette treatment for a commercial launch without addressing those terms. Neutral ink/paper were added for contrast.
- Real component: Dillion Verma’s **Number Ticker**, listed at https://21st.dev/@dillionverma/components/number-ticker and obtained from the public Magic UI upstream. Its source is bundled, not a visual imitation. Its original MIT licence is retained in the HTML. The public component route does not consume your paid 21st.dev account.
- Mobbin paid screenshots were not accessible from any agent browser (three environments checked); the layout uses your written descriptions plus your three screen recordings (Rivian hero, Humble timeline, Atlas process — received 7 Nov 2026). No claim of a pixel-exact reproduction. The hero word-cycle timing ports your supplied Animated Text Cycle source (thimows, 21st.dev): 5s interval, 0.3s easeIn exit, 0.4s easeOut enter, ±20px y, 8px blur. No width spring is used — the word sits alone on its line, so reflow is equivalent.
- Existing CAD source: https://agibalya2b.github.io/alphaplus-ar/ — A. Omar / Team 4, form-and-fit prototype, not production intent. The animated SVG is a separate simplified explanatory schematic.
- Barlow Condensed display, Manrope body, IBM Plex Mono utility fonts. GSAP ScrollTrigger plus Motion for React drive the live motion. No analytics.

## Final submission checks

Supply the **film and captions, five names, full-model URL, supplier evidence, interview references and dated retail-price evidence**. Then test at the projector resolution and on a phone. Test the optional AR flow on an actual supported phone; desktop rendering cannot verify AR operation. Confirm the entire film plays and captions match in your target browser. The course site is deliberately not represented as a launched, RTA-approved or production-certified service.

Build checks: four service steps, five comparison rows, four rollout stages, five named placeholders, matching visible/data figure values, unique HTML IDs and valid internal anchors. The six principal body-text colour pairs were calculated at 4.64:1 or higher. Desktop and phone hosted captures were inspected. A long mobile capture showed stripe artifacts around the financial section; a separate same-code financial-section render showed the complete caption and source without striping, so this remains a full-page-capture limitation rather than a confirmed browser defect. No local interactive browser/AR test was available; check presenter keys, motion, dialogs, film playback and the 3D viewer on the actual webinar laptop and phone before presenting.

## Changes, 7 Nov 2026 (Team 4)

- On-screen caveats shortened to one source line per figure; detail stays in the Sources dialog and details panels.
- Five team names added; model v4 linked (`assets/Path_A_model_v4.xlsx`); model assumptions and sensitivities written into the details panel.
- Environmental claim restored with the uses-to-return-rate conversion shown.
- Supplier, interview and in-store price sources named; closed-drink rule reading added.
- No changes to layout, motion or script.

## Changes, 7 Nov 2026 (v3 motion layer and Tweaks)

- Hero: the Borrow / Return / Repeat word now dissolves into dust and the next word rises letter by letter, on a loop (after the Rivian recording).
- Problem: a split-flap morning board replaces the three counters (vanilla port of the 21st.dev Split Flap Departure Board by f0rextasy, MIT; layout after Railway on Mobbin). One row re-flaps every 7 seconds. "Free hands: 0" is labelled as the persona scenario.
- How it works: a large outline word (FILL, DOCK, PAUSE, RETURN) slides across the drawing for each step, with step dots (after Atlas), plus a coral progress rail and filled step tags (after Humble).
- Section headings come into focus from a blur when they reach the viewport.
- Recommendation: a light pulse runs along the line and stations light up in order.
- Closing: an infinite Borrow. Return. Repeat. marquee.
- Tweaks panel (top bar): palette presets (Ocean Five, Thought Provoking), nine colour pickers, display / body / mono fonts from Google Fonts, headline size, effects on or off. Settings stay in the browser; Copy CSS gives a :root block to paste in permanently.
- All colours and fonts now run through CSS variables, including derived greys (color-mix of ink and paper) and the inline SVG colours.
- Motion respects the Motion toggle and reduced-motion settings.

## Changes, 7 Nov 2026 (v3, results and closing)

- Is it worth it: a big-number stage replaces the three metric cards (after Stripe on Mobbin). It cycles NPV (AED +2.55M), break-even (~17 months) and menu price (AED 17) every 5.5 s, with a count-up, a flowing line wave in the palette colours, previous/next buttons and progress bars. Hover or focus pauses it.
- Count-ups (Number Ticker timing) on the hurdles (~221 / day, ≥82%) and a new 97.5% figure in the carbon card.
- Three number treatments now: split-flap board (Problem), big-number stage (Worth), count-ups (hurdles, carbon, closing counters).
- Closing: Slack-style headline with floating counters (free hands 2, paper bags 0, deposit back AED 26, return target 97.5%); Melius-style curved panel whose curve breathes, with a line that draws itself between "Start small," and "prove the loop."
- Footer: Melius-style giant alpha+ wordmark on a dot grid with a light sweeping through the letters (follows the pointer on desktop), behind a dark footer card.

## Fixes, 7 Nov 2026 (after Ahmed's review)

- How it works: the sliding word (FILL, DOCK, PAUSE, RETURN) now has its own strip between the drawing and the caption, sized to the drawing, so it no longer overlaps labels; the drawing is no longer clipped, so the strap clip stays visible in every step. Hidden on phones, where the drawing is small.
- Comparison: each row now reveals over 2.4 s, one row after another.
- Footer: the alpha+ wordmark is fully visible above the credits card.
- Team photos: five photo slots. Add photos to assets/team/ as ahmed-omar.jpg, jane-macgregor.jpg, omer-uner.jpg, englebert-zoa-etundi.jpg, jonathan-salmeron.jpg (portrait, 4:5). Initials show until a photo is there.

## Change, 7 Nov 2026: station permission reframed

- The "No permit. No pilot." hard-stop box is replaced by the station precedent the team already found: cafés trading in station units before the gates (Sharetea BurJuman, Sunda Café and Alcatraz Café Emirates Towers, Slims Café Dubai Internet City, Tea Station Al Furjan; Google Maps listings, 30 Oct 2026) and Choithrams Quickerr selling food and beverages at Abu Hail, Stadium, Al Nahda and DAFZA (Gulf News, Aug 2026).
- Pilot step zero is now "lease a unit whose RTA listing allows food and drink" (RTA "Invest with RTA" listings state the activities not allowed per unit; Khaleej Times, Oct 2025).
- Same reframing in the rules panel, the Pilot station card and the Sources dialog.

## Fixes, 7 Nov 2026 (second check)

- Drawing: the collar and strap clip are now drawn in front of the steel body, so the blue part is never covered; extra room under the drawing so the pod never touches the step word.
- Comparison: the table now reveals row by row in a strict sequence (1.5 s per row, next row starts as the previous one finishes; about 7.5 s for all five), triggered once when the table is in view.
- Worth it: the big-number stage loops on its own with no arrows, 9 s per number (pauses while hovered).

## Change, 7 Nov 2026: Metro-only ridership

- The 2025 all-modes figure (802.1M rides across public transport, shared mobility and taxis) is replaced by Dubai Metro only, January to June 2026: 136.5M rides (Dubai Media Office / RTA, 2 Aug 2026). About 754,000 a day; BurJuman 8.4M, about 46,400 a day (Team 4 calculation over 181 days).
- Morning board widened to 26 cells for "METRO H1 2026 136,500,000".

- "What must be true": the 221 / day hurdle is set against BurJuman traffic (about 0.50f 46,400 daily rides) and the UK station benchmark (about 2.50f visits buy coffee; Network Rail, Q1 2015-16, Team 4 calculation).

## Changes, 9 Nov 2026 (v4, team meetup decisions)

- Model v5 (`assets/Alpha_Plus_model_v5.xlsx`): base return rate 90%, the team's pilot target. NPV AED +2.60M; break-even about month 17. One change at a time: menu AED 16 +2.11M; ingredients 35% +1.12M; no lost-vessel deposits kept +1.08M.
- Journey steps named as need → answer pairs: HOLD → SEAL, TAP → DOCK, SAVOUR → PAUSE, GO LIGHT → RETURN.
- Environmental card: 40–50 uses for a steel cup to beat a paper cup on CO₂; claim less waste now and a CO₂ reduction as returns climb, measured in the pilot. Closing chip: return target 90%.
- Persona quote from Jane; comparison intro from Ömer ("Designed around the commute, not around the cup."); about 20 seconds per no-milk espresso drink at the kiosk; parts-cost line.
- Top bar: 80% ink background with the logo, title and progress bar only. Tweaks open with `?tweaks` in the address.
- Film: if it had to start muted, sound turns on at the first click, tap or key press.
