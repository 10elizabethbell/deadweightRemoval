# Deadweight Removal — handoff at ~60%

**Live:** https://10elizabethbell.github.io/deadweightRemoval/ · **Repo:** https://github.com/10elizabethbell/deadweightRemoval · **Built:** 2026-10-08 from Muse brief (Muse run 2026-10-08, Marlton NJ Local Business Group flyer post)

## What's built
- **One page, phone first:** top bar (wordmark + tap-to-call number top right), hero (headline, one promise line, one Text a photo button), "What we haul" (6 services as short names), "Photo to gone" (3 steps), the flyer's promises on an electric-blue band, "Before & after" (two drag sliders and one cleared-garage photo, then a "See our Facebook for more of our work" button), closing section with name, area and Text button, footer with name, area, number and Facebook.
- **World:** the client's own logo and their real trailers. Household junk, snapped steel chains, electric blue, navy night. Navy ground (`#0f1b30`, never black), steel-light services section, blue promise band. System fonts, heavy uppercase display.
- **Signature element:** a junk pile along the bottom of the hero and the close (boxes, trash bags, tires, chairs, couches, mattresses, pallets, bins, TVs, buckets, branches, washers, all drawn in code). The surface rolls, mouse or finger shoves junk around with a spring wobble, and a tap or upward swipe flings pieces up; they fall back into the heap. In the hero, a worker walks from the pile to a pickup and black dump trailer (logo on the side, red/white tape, after Ellie's reference photos), picks junk up, carries it overhead and tosses it in. The mouse jumbles the load and can knock pieces out onto the ground; he fetches those first. When the trailer is full the truck drives off and backs in empty. Tunables: `DW.junk` and `DW.crew`. The real logo, cut out of its dark square with an alpha matte (`src-assets/logo-cut.png`, not committed), stands *in* the pile: back rows behind it, front rows in front. Blue dust motes rise and dodge the pointer.
- **Chain seams:** every section boundary is a sagging, rippling steel chain (alternating ring and edge-on links) and the next section's color fills below the moving chain. Pushing it with a finger sends a wave along it. Below both piles the chain lies across the pile's base: the seam's top half is transparent.
- **Contact:** every action uses 609-852-8552. "Text a photo" opens SMS with a pre-filled quote request (What needs to go / Town / When works / I'll attach a photo). Each service row texts with that service named. Calling is the header's top-right number (`tel:`), plus inline links in step 2 and the footer; no Call buttons and no sticky bar. On desktop the close button shows the number, and hovering a service updates a text-message preview card.
- **Favicon and home-screen icon** are the strongman and diamond cropped from the logo (`favicon-32.png`, `apple-touch-icon.png`). **Link preview:** `og-image.jpg` (1200×630, logo on navy), with `og:url` pointing at the Pages site.
- **Hero drag:** on phones the hero pile takes vertical drags too (`touch-action:none` on it, pull-to-refresh off); scroll by swiping the text above it.
- Tunables are at the top of the `<script>` in `DW` (lanes, sizes, push, kick, chain speed and sag).

## Assumptions I made
- **Headline "Drop the dead weight."** is a play on their name, not their wording.
- **Colors** were sampled from the logo (blue `#2694f1`/`#156ed0`, navy glow `#10192a`). Their real brand colors are unknown.
- **Service one-liners** ("Couches, tables, dressers", "Washers, dryers, fridges", "Branches, brush, leaves and clippings") are my plain-language examples of their flyer categories. The reviewer cut mattresses and stoves (often surcharged or refused); ask before adding them back.
- **Hero promise** ("We come when it suits you, treat your home with care, and leave nothing behind but the space you wanted back.") is written about how they treat the customer, built on their "flexible scheduling" and "reliable & professional". The care and clean-exit parts are my wording, not theirs; confirm with the owner.
- **"We" voice:** crew size is unknown, so the page says "we". Switch to "I" if it's one person.
- **"Text it for a quote"**: the flyer says "call or text". That they quote from a photo is Muse's inference (a natural fit for junk), not stated by them.
- **"5% off for cash"** paraphrases the flyer's "5% DISCOUNT CASH". The promise band uses their wording verbatim, with "Reliable & professional" as its first line.
- **Step 3, "You point, we load it and take it away"**, assumes they do the loading (standard for junk removal, not stated).
- **Area** is "South Jersey & surrounding areas" (flyer). Marlton/Burlington County is only where the post was found, so no towns are listed.

## Placeholders and gaps
- **Work photos** (5, supplied by Ellie 2026-10-17): two garage before/after pairs, aligned on the back wall and cropped 4:5 into `img/` (800px WebP); the third is an after shot looking out at the loaded trailer, with the person by the car blurred. Raw originals are in `src-assets/` (ignored). Framed family photos in one after shot fall outside the crop.
- **Flyer image not obtained:** it needs a logged-in Facebook browser (the og:image of the group post is the group's Marlton clock cover). So **"FREE ESTIMATES" is not on the page**, as Muse advised. If the flyer confirms it, add it to the perks and the promise band.
- No hours, no owner name, no email, no reviews, no prices. None of these appear on the page. When there's an email, it goes in the footer only.
- **Facebook link** goes to page ID 61587889134420 from the brief. That page is restricted to logged-out viewers, so I couldn't check that it shows their work. The button sits right under the before/after photos.
- The logo is a 720px Facebook profile image, cut out and embedded at 576px WebP (47KB, most of the 107KB page). Ask for the original file; a vector would be lighter and sharper.
- The hero's proof chips (Same day / Insured / 5% off) were cut for a single focal point; the promise band still says all three.

## Questions for the owner
- Do you give free estimates? (The flyer OCR read "FREE ESTIMATESE".)
- Hours? Is same-day subject to a cutoff time?
- Which towns do you cover most? Is there a mileage limit?
- Photos: loaded truck, before/after of a cleanout, the crew (if they want faces online).
- Anything you *don't* take (paint, tires, hazmat)?
- What's your first name, for "Text Mike a photo"-style copy?
- Do you have a real brand color, or is the logo's blue it?

## Ideas not built (yours to pick)
- **The chain snaps** (from the finish review): shove a seam hard enough and it breaks with a blue spark and throws links, then re-links. It's the logo's own gesture and the strongest next step for the signature.
- **The close finishes the story** rather than repeating the hero: the closing pile mostly hauled away, a few pieces left, or the truck driving off full.
- **Desktop text preview card** is plain white iMessage-style. It could take the world's steel and navy instead.
- **Promise band on desktop** wraps in a two-column grid with a big gap; a single column or a marquee may read better.
- **Runner-up world: "Snap the chains."** Swinging steel chains hang from the top of the hero (verlet rope physics). Drag one hard enough and it snaps with a blue spark, echoing the logo's strongman. The pile is more "junk"; chains are more "brand".
- **Booking form page** (`book.html`) composing the same text: item type, size (single item / half truck / full truck), town, day, time window.
- **Truck-load size picker** ("¼ / ½ / full truck") that fills the hero trailer to that level. Only if they price by load.
- Promise band could get a slowly scrolling marquee of the flyer lines.
- Copy alternatives for the headline: "Your junk. Gone same day." / "We haul the dead weight."

## Not verified
- Real-device touch feel (headless touch and mouse sweeps both move the pile and chains; flick-to-break-free not felt on glass). The hero pile blocking scroll on phones is per the finishing rules; check it doesn't feel stuck.
- The real SMS handoff on iOS and Android, especially from inside Facebook's in-app browser. The `sms:+1…?&body=` form is the cross-platform one, but untested on devices.
- Frame rate on older phones (junk pile, crew + 5 chain seams; everything pauses off screen).
- Reduced-motion still frame (code path exists, not screenshotted).
- The concept-roll seed step of Impeccable's new-work flow was skipped: the build ran unattended per the pitch-site skill, and the world was chosen from the brief and logo without the interactive decision page.
