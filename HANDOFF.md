# Deadweight Removal — handoff at ~60%

**Live file:** index.html · **Repo:** https://github.com/10elizabethbell/deadweightRemoval · **Built:** 2026-10-08 from Muse brief (Muse run 2026-10-08, Marlton NJ Local Business Group flyer post)

## What's built
- **One page, phone first:** top bar (wordmark + tap-to-call number), hero, "What we haul" (6 services), "Photo to gone" (3 steps), the flyer's promises on an electric-blue band, closing section with name + area, footer with "Demo one-pager — free sample."
- **World:** the client's own logo. Chiseled concrete chunks, snapped steel chains, electric blue, navy night. Navy ground (`#0f1b30`, never black), steel-light services section, blue promise band. System fonts, heavy uppercase display.
- **Signature element:** a rubble pile along the bottom of the hero and the close, about 230 chunks on phones and 750 on desktop, drawn as shaded solid blocks. The pile's surface rolls, mouse or finger shoves chunks around with a spring wobble, and a tap or upward swipe flings top chunks clear: they lift away, fade into dust, and fresh junk drops back in. The real logo, cut out of its dark square with an alpha matte (`src-assets/logo-cut.png`, not committed), stands *in* the pile: back rows behind it, front rows in front. Blue dust motes rise and dodge the pointer.
- **Chain seams:** every section boundary is a sagging, rippling steel chain (alternating ring and edge-on links) and the next section's color fills below the moving chain. Pushing it with a finger sends a wave along it. Below both piles the chain lies across the pile's base: the seam's top half is transparent.
- **Contact:** every action uses 609-852-8552. "Text a photo" opens SMS with a pre-filled quote request (What needs to go / Town / When works / I'll attach a photo). Each service row texts with that service named. Call buttons use `tel:`. A sticky Text/Call dock appears on phones once the hero buttons scroll away, and hides again at the closing buttons. On desktop the buttons show the number, and hovering a service updates a text-message preview card.
- Tunables are at the top of the `<script>` in `DW` (lanes, sizes, push, kick, chain speed and sag).

## Assumptions I made
- **Headline "Drop the dead weight."** is a play on their name, not their wording.
- **Colors** were sampled from the logo (blue `#2694f1`/`#156ed0`, navy glow `#10192a`). Their real brand colors are unknown.
- **Service one-liners** ("Couches, tables, dressers", "Washers, dryers, fridges", "Branches, brush, leaves and clippings") are my plain-language examples of their flyer categories. The reviewer cut mattresses and stoves (often surcharged or refused); ask before adding them back.
- **"Text it for a quote"**: the flyer says "call or text". That they quote from a photo is Muse's inference (a natural fit for junk), not stated by them.
- **"5% off for cash"** paraphrases the flyer's "5% DISCOUNT CASH". The promise band uses their wording verbatim, with "Reliable & professional" as its first line.
- **Step 3, "You point, we load it and take it away"**, assumes they do the loading (standard for junk removal, not stated).
- **Area** is "South Jersey & surrounding areas" (flyer). Marlton/Burlington County is only where the post was found, so no towns are listed.

## Placeholders and gaps
- **No work photos or before/afters.** The page leans on the motion and typography instead. Real truck/pile/cleared-basement shots would be the biggest upgrade.
- **Flyer image not obtained:** it needs a logged-in Facebook browser (the og:image of the group post is the group's Marlton clock cover). So **"FREE ESTIMATES" is not on the page**, as Muse advised. If the flyer confirms it, add it to the perks and the promise band.
- No hours, no owner name, no email, no reviews, no prices. None of these appear on the page.
- No `og:image` for link previews (a data URI can't be one). Add a hosted 1200×630 share image once there's a URL.
- The logo is a 720px Facebook profile image, cut out and embedded at 576px WebP (47KB, most of the 107KB page). Ask for the original file; a vector would be lighter and sharper.
- At a realistic Facebook in-app height (390×664) the first screen shows the headline, pitch, both buttons and the proof chips; the logo and pile start right at the fold. To pull the logo up you'd have to shrink something above it. Your call.

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
- **The close finishes the story** rather than repeating the hero: the closing pile mostly hauled away, a few chunks left.
- **Desktop text preview card** is plain white iMessage-style. It could take the world's steel and navy instead.
- **Promise band on desktop** wraps in a two-column grid with a big gap; a single column or a marquee may read better.
- **Runner-up world: "Snap the chains."** Swinging steel chains hang from the top of the hero (verlet rope physics). Drag one hard enough and it snaps with a blue spark, echoing the logo's strongman. The pile is more "junk"; chains are more "brand".
- **Rubble that drains:** a "clear it" moment where scrolling into the close section empties the pile (haul-away), then it refills.
- **Before/after sliders** once they send cleanout photos (taste section 4).
- **Booking form page** (`book.html`) composing the same text: item type, size (single item / half truck / full truck), town, day, time window.
- **Truck-load size picker** ("¼ / ½ / full truck") that fills a little truck bed with rubble. Only if they price by load.
- Promise band could get a slowly scrolling marquee of the flyer lines.
- Copy alternatives for the headline: "Your junk. Gone same day." / "We haul the dead weight."

## Not verified
- Real-device touch feel (headless touch and mouse sweeps both move the pile and chains; flick-to-break-free not felt on glass).
- The real SMS handoff on iOS and Android, especially from inside Facebook's in-app browser. The `sms:+1…?&body=` form is the cross-platform one, but untested on devices.
- Frame rate on older phones (~230 chunks + 4 chain seams; everything pauses off screen).
- Reduced-motion still frame (code path exists, not screenshotted).
- The concept-roll seed step of Impeccable's new-work flow was skipped: the build ran unattended per the pitch-site skill, and the world was chosen from the brief and logo without the interactive decision page.
