# Email list cleanup deck (Javier's own presentation)

**Built 2026-10-14.** Javier sent Alex Hormozi's ACQ Vantage "Clean Your Email List" Quick Wins training
(Downloads mp4, 10:40) and asked to remake the slides as his own presentation on email decay: "make it seem like I wrote it."

- Live: https://javmartz04-ship-it.github.io/email-decay-deck/ (repo javmartz04-ship-it/email-decay-deck, push to update)
- Single `index.html`, 1920x1080 stage. Arrows/space/click, F = full screen, N = speaker notes, `#N` deep-links.
- Register: the whiteboard teaching style approved on the RIG Marketing Machine deck (Inter Tight 800 + yellow
  highlighter, Caveat pen notes, hard offset shadow tiles), dark photo openers. Mono for the prompt.
- Photos: Pexels 20234204 (fridge at night), 6934545 (rotten apple).

## What changed from the source
- All ACQ / Acquisition.com / Hormozi branding, the Miroslav shout-out, "pay for this program" PS, "ACQ AI" and
  "comment below the post" removed. AI = "ChatGPT or Claude". Every line reworded; structure kept.
- 27 source slides -> 17. Fridge illustration redrawn as SVG line art with labels; vicious cycle and before/after as real diagrams.
- Decay numbers are Alex's spoken figures (100 -> 77 -> 59 still responding after years 1 and 2). Unsourced; flagged to Javier.
- Added two transcript points: "rent is due every day" and "your list can't be too clean" (new excuse row).
- Speaker notes written in Javier's voice from the transcript.

## Craft bugs hit
- `.rise` sets `transform:none` on active slides, so a `transform:scale()` on the same element silently did nothing.
  Put scale on a child of the `.rise` wrapper.
- Bold spans inside a `display:flex` table cell become separate flex items and lose their spaces. Use block.

## v2 · Brandridge brand pass (2026-10-14)
Javier sent his Brandridge logo: "Use my premium brand colors, make it super premium."
- Colors sampled from the logo: #001DFB → #0181FC → #0AEBFF, stripe navy #030D30, black, white.
- Logo traced to SVG with potrace (6x upscale, blue channel threshold; silhouette in navy + gradient body on top so the
  ridge stripe stays navy on any ground). Note potrace's y-flip: the gradient needs x1=0 y1=0 x2=1 y2=1 to run bottom-left → top-right.
- Whiteboard v1 kept locally as index.v1-whiteboard.html (gitignored).
- Bug: `.rise` owns `transform`, so `translateY(-50%)` centering on a rising element is dropped. Position with top instead.
