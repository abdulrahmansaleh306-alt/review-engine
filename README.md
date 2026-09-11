# Review Engine — landing page

My own sales page. A one-page site with online booking wired into it, which is
also the demo of the exact thing I sell to clients.

**Live:** https://abdulrahmansaleh306-alt.github.io/review-engine/

## Files

| File | What it is |
|---|---|
| `index.html` | All the text. This is the file to edit. |
| `styles.css` | Colours, fonts, spacing. Rarely needs touching. |
| `logo.png` | The Review Engine mark. |

No build step, no install. Open `index.html` in a browser and it works.

## Connecting the booking

At the bottom of `index.html`:

```js
var CAL_LINK = "";
```

Put your Cal.com booking link between the quotes — just the path, no domain:

```
booking page:  cal.com/abdulrahman/15min
you write:     "abdulrahman/15min"
```

Leave it empty and the page shows a WhatsApp button instead. That's the
fallback, so the page is never broken while the booking isn't set up.

## Setting up Cal.com (once)

1. Sign up free at cal.com
2. Connect Google Calendar when it asks — this is what stops double-booking
3. Create an event type (e.g. a 15-minute call)
4. Copy the booking link it gives you
5. Paste the path into `CAL_LINK` above

The free plan covers unlimited event types and unlimited calendar connections.

## Reusing this for a client

Each client gets **their own** free Cal.com account, created in their name and
connected to their own Google Calendar. Their bookings and their customers'
details stay in their account, not mine — so nothing is mine to lose, and they
keep everything if we stop working together.

Then: copy this folder, swap the text, set `CAL_LINK` to their link, push to a
new repo, enable Pages, point their domain at it.

## Design notes

Monochrome, taken from the logo: flat black on warm off-white (`#f2f0ec`), with
one accent (`#b5241a`) used only on the free-offer badge. Black Ops One is the
logo's own typeface, used for Latin labels and numbers. Arabic is Tajawal for
headings and IBM Plex Sans Arabic for body. Page is right-to-left.

Structure follows the landing page notes in `../transcripts/`: headline promises
the outcome, sub-headline answers the biggest doubt, pain section sits directly
under the fold, and the three objection blocks are ordered most common first.
