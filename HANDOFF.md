# Little Diggers Construction — handoff at ~60%

**Live:** https://10elizabethbell.github.io/littleDiggersConstruction/ · **Repo:** https://github.com/10elizabethbell/littleDiggersConstruction · **Built:** 2026-10-19 from the Muse brief of 2026-10-19 (found via the "Essex County Contractor Referrals" group post)

## What's built
- One page, phone first: header (wordmark, `508-917-6408` top right), hero, What we do, Fresh off the job, How a job goes, Tell us about your job (quote form), footer.
- **World: "marked out before the dig."** The ground is wet loam brown and the sections in between are speckled granite with a curb edge. Utility locate paint (blue water, yellow gas, green sewer, red electric) is sprayed on the lawn and under each heading. White marking paint frames the photos at the corners, and grass fringes grow where soil meets stone.
- **Signature element:** the hero lawn is a canvas you dig with a finger or mouse in any direction. Grass parts around the pointer, dirt clods fly out and land on the lawn, and each paint mark has the matching pipe under it (sand bedding and all). The hole fills back in after a few seconds. Until someone touches it, the lawn digs itself along one mark after another. Grass sways all the time, and the fringes sway and part too. One shared animation loop pauses whatever is off screen. With reduced motion everything stays still, but digging still works.
- **Contact:** the phone number is a `tel:` link in the top right. The hero has two buttons: Get a quote (to the form) and See our work. Tapping a service row jumps to the form with that service already ticked. The form builds a text to `+15089176408` (`sms:` link with an encoded body) and also shows the message with a copy button and the phone number, for desktops and in case texting doesn't work.
- The Facebook button ("Click to see more of our work.") sits under the photos, and Facebook is also in the footer. There's no email anywhere, because none exists.
- The favicon and home-screen icon are "LD" in the site's own lettering. `og.jpg` (1200x630) is the headline next to the granite stairs photo.

## Assumptions I made
- **Colors:** there's no logo or brand color. Machine yellow comes from the Deere dozer in their own photo. Loam brown, granite gray and lawn green come from the work itself. Survey-flag pink is the form highlight.
- **Voice:** "we" (a crew: "The guys killed this stairway…"). Mark is named as owner because the Facebook page says so.
- **Headline:** "Dug right. Left clean." and the promise ("works your yard like it's our own… leave it better than we found it") are written by me, not quoted. They're about care, not credentials.
- **How a job goes**, step 2 ("We walk the site with you… give you a straight price") is inferred. Confirm they do site visits and quotes this way.
- **Service label:** I wrote "Underground utilities" with the correct spelling. The brief asked to keep their spelling "utilitys" verbatim; that applies to quoting their caption, and their caption isn't quoted anywhere on the page. Change it back if you'd rather.
- **Address:** only "Auburn, Massachusetts" is shown (their Facebook page confirms Auburn). I didn't publish the 165 South St address, because their own page doesn't confirm it.
- **Texting:** whether they take texts is unknown. The quote form hands off by text, and calling sits beside it every time (header, form help line, step 1, footer).

## Placeholders and gaps
- Only **two photos**: the granite stairway (cropped from the job video thumbnail, with the music sticker and blurry foreground removed) and the dozer grading shot (their Facebook profile photo). There are no before/afters.
- No logo, so the wordmark is set in the system font.
- No hours, reviews, prices, licence or insurance, years in business, or email. None of these are on the page.
- The stairway **video** itself isn't embedded (it needs a logged-in download).

## Questions for the owner
- Do you take texts at 508-917-6408?
- Can we have 6–10 more job photos, ideally before/after pairs (stairs, trenches, grading, walls)?
- Which towns do you cover around Auburn?
- Do you do free estimates or site visits? Any hours to list?
- Licensed or insured? Anything you'd like to say about that (only with proof)?
- Do you have a logo, or a truck or sign with your colors?
- Do you want the "we have some openings" message on the site when you have them?

## Ideas not built (yours to pick)
- **Runner-up world:** a granite quarry or split-face stone world (drill-hole feather marks, split granite blocks as section edges, stone that cracks apart under the finger). Stronger for a stairs-first pitch, weaker for excavation.
- A "We have openings this month" strip that Mark can switch on and off (from their own "WE HAVE SOME OPENINGS…" post).
- Before/after sliders under each service once pairs exist.
- Embed the stairway job video (muted, loops, tap to play) in Fresh off the job.
- A drag hint that fades after the first dig. A small digger-bucket shadow that follows the self-dig, so it reads as a machine at work.
- A separate quote page with photo attachments (MMS can't be pre-filled; this would need a backend or an email service).

## Not verified
- Real-device touch on iPhone and Android, inside Facebook's in-app browser (tested only with simulated pointer and touch events in headless Chrome).
- The `sms:` hand-off on real iOS and Android (`?&body=` form).
- Frame rate on old phones (phones get about 2,300 blades, desktop about 5,800).
- How the SVG spray filter renders on iOS Safari (it's on SVG elements, which should be supported).
