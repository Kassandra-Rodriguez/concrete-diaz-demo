# Concrete Diaz — concept site

Speculative one-page lead-gen site for **Concrete Diaz** (Concreto Diaz LLC), El Paso, TX
and southern New Mexico, from the El Paso pipeline. Built 2026-09-05, adapted from
`quamcrete-demo` with an orange reskin. Static site, no build step: `index.html` +
`styles.css` + `script.js` + `assets/`.

Research notes: `RESEARCH.md`. Photo brief: `PHOTO-BRIEF.md`.

## The hook (for outreach)

**This is an "upgrade" pitch, not a "you have no website" pitch.** Concrete Diaz already
has `concretediaz.com` (a parallax one-pager with a family-owned story, a gallery, and a
6-field contact form), linked twice from their Facebook. So the angle is:

> The site exists, but the quote path is buried. The hero is a slogan, not a form. "Get in
> Touch" scrolls you to the very bottom past a wall of text before you can ask for
> anything. Their Meta ads (Spanish, owner on camera) still dead-end in Messenger instead
> of pointing at a page. This demo makes "get a free quote" the obvious action in the
> hero, in the sticky mobile bar, and at the end of every section, adds a real project
> gallery and a financing calculator (their ads push "bad credit approved"), and ships
> bilingual because 100% of their ads are in Spanish.

## Verified vs placeholder

| On the page | Status | Source / note |
|---|---|---|
| Name "Concrete Diaz" / Concreto Diaz LLC | Verified | Facebook, BBB, concretediaz.com |
| Phone **(915) 242-3657** (tel/sms, forms, footer) | Verified | Facebook "Contact info" (mobile + WhatsApp), matches prospect sheet |
| Email concretediaz.ep@gmail.com | Verified | Facebook "Contact info" |
| Instagram @concrete.diaz, Facebook /concrete.diaz.ep | Verified | their pages |
| **BBB Accredited** (trust bar, footer) | Verified as accredited | BBB profile: business started 5/22/2024, BBB Accredited since 5/8/2025. **The letter grade ("A") is from the prospect sheet and was not re-confirmed — say "BBB Accredited" only, or verify the grade before send.** |
| "Family owned and run" / "the owner is on your job" | Verified-ish | concretediaz.com says "family-owned and operated"; owner Jesus Jared Diaz Izaguirre (BBB). "Owner on every job" is a fair read, not a direct quote. |
| Services: driveways, patios, slabs, foundations, stamped/decorative, sidewalks, steps, block & retaining walls, stone veneer, custom gates, pergolas, turf, tear-out | Verified | Facebook bio + concretediaz.com ("driveways, patios, foundations, slabs, custom") + their photos (gates, stone veneer, pergolas, stamped, turf) |
| Service area: El Paso metro + Chaparral / Sunland Park / Anthony NM | Verified-ish | Facebook lists "Las Cruces, NM · El Paso, TX"; watermark address is Chaparral, NM. Checklist neighborhoods (West Side, Upper Valley, etc.) are the standard El Paso list — confirm the real radius. |
| **Financing** section + calculator (11.99% APR, 12/24/36 mo, $2k–$20k) | **Placeholder math** | They advertise financing / "bad credit approved" in their Meta ads, so the section is justified, but the **APR, terms and monthly figures are invented**. Confirm the real lender/terms, or cut the calculator and keep just "financing available". |
| Bilingual EN/ES (full site) | **Our addition, needs a native check** | Their ads are Spanish, their site is English. The `data-es` copy is our translation. |
| Business hours ("Open by appointment", "confirm hours") | **Placeholder** | Facebook only says "Always open". |
| Years in business, crew size, licensed/insured/bonded | **Not on the page** | Founded 2024 (~1 yr). Left off deliberately — a "new but accredited" business leads with BBB + workmanship, not tenure. Add "insured" etc. only if confirmed. |
| No street address on the page | Deliberate | Watermark shows 471 Dorado, Chaparral, NM 88081, but that reads as a home/registration address, not a shop. Treated as a service-area business (photo + coverage checklist, no map), per the pipeline rule for address-less businesses. |
| Star ratings / review counts | **Not on the page, do not add** | Facebook shows "Not yet rated (0 reviews)". No social proof exists yet — the no-fabrication rule applies. Trust bar uses BBB / financing / free estimate / family-run instead. |

## Photo mapping

All 8 photos are **real Concrete Diaz work**, supplied by Kassandra from their
Facebook/Instagram into `assets/originals/`. Optimized copies (resized, watermarks
cropped off where they sat in a dead zone) are what the page loads.

| File on page | From `originals/` | Shows | Used as |
|---|---|---|---|
| `hero.jpg` | `concrete2.jpg` (crop) | stamped flagstone walkway + brick circle inlay + turf | hero background |
| `g1-stamped.jpg` | `concrete2.jpg` (crop) | same, framed lower to show the stamp + inlay | carousel |
| `g2-patio-pergola.jpg` | `concrete3.jpg` (crop) | stamped slate patio under a louvered pergola | carousel + service-area photo |
| `g3-turf-walkway.jpg` | `concrete.jpg` (crop) | concrete borders + paver stepping-stone path around new turf | carousel |
| `g4-gate.jpg` | `gate2.jpg` | black louver double gate on stone-veneer posts | carousel |
| `g5-privacy-wall.jpg` | `gate.jpg` | black woven-steel privacy wall, Franklin Mtns behind | carousel |
| `g6-wood-gate.jpg` | `gate3.jpg` | cedar-and-steel double gate | carousel |
| `g7-pergola.jpg` | `pergola.jpg` (crop) | louvered pergola over a stone-veneer wall | carousel |
| `g8-stone-wall.jpg` | `screen.jpg` | stone-veneer wall going up on set steel posts (mid-build) | carousel |

**No matched before/after pair exists** in the set, so the template's before/after slider
was removed. A real "dirt lot → finished" pair of the *same* job would be a strong add
(see `PHOTO-BRIEF.md`). Watermark remnants: a faint hose-reel edge on `g1`/hero and a
few px of logo top on `g2` may still be visible at some crops; re-crop from `originals/`
if it bothers you.

## Logo

Kassandra supplied the real logo as `assets/logo.jpg` (full lockup, orange on white).
From it:

- `assets/logo-mark.png` — the monogram only, white knocked out to transparent, RGB
  flattened to the brand orange. Used in the header and hero (on dark).
- `assets/logo-lockup.png` — monogram + "CONCRETE DIAZ" wordmark, same treatment. Used
  in the footer.

The generator: `assets/originals/logo-fb-lockup.jpg` is the untouched source; the crop
boxes and the luminance→alpha ramp are in the shell history (PIL, `python3.11`). If a
higher-res or vector logo turns up, redo those two PNGs the same way. The interior negative
space of the monogram is transparent by design, so the dark background shows through it,
same as the real logo on their Facebook cover.

## Palette & type

Orange reskin on a warm near-black ground, with concrete-grey light sections for contrast.

```
--bg          #0c0b0a   warm near-black ground
--accent      #e96d49   brand orange — sampled from assets/logo.jpg (median of the flat orange)
--accent-300  #f3a184   light orange — eyebrows / accents on dark
--accent-ink  #bf4f2a   burnt orange — accents on light sections
--light       #f3f2f0   concrete-grey light-section ground
--ok          #4da65f   green — "free / go" cue
```

Section rhythm: dark hero + trust bar, dark "what we build", **light** work gallery,
dark "how we pour", warm-dark financing, **light** service area, **orange** final CTA,
near-black footer.

Type: **Sora** (headings) + **Manrope** (body), Google Fonts. If the owner wants a
different look, revisit palette/type with Mobbin references first.

## Not yet done

- **Mobile QA on a real device.** This machine floors small viewports, so the phone
  layout is inherited-from-`quamcrete-demo` and only assumed correct: the services grid
  and the "how we pour" steps collapse to horizontal swipe rows at <=640px, the hero
  quote form collapses behind a "Start my quote" button, the header CTA hides and the
  sticky bottom bar takes over. Worth a true ~390px pass.
- **Confirm before send:** BBB letter grade, financing APR/terms (or cut the calculator),
  Spanish copy (native check), business hours, the service-area radius, and that every
  photo is their own work (all 8 look like El Paso / Chaparral, so this is low risk).
- Live check that GitHub Pages serves the fonts and all `assets/` images.

## Hosting

Private repo first, then Kassandra runs (the assistant is blocked from these):

```
gh repo edit Kassandra-Rodriguez/concrete-diaz-demo --visibility public --accept-visibility-change-consequences
gh api --method POST /repos/Kassandra-Rodriguez/concrete-diaz-demo/pages -f "source[branch]=main" -f "source[path]=/"
```

Live ~1 min later at `https://kassandra-rodriguez.github.io/concrete-diaz-demo/`.
`<meta name="robots" content="noindex, nofollow">` is set so it will not compete with
`concretediaz.com` while it is a concept.

## Outreach talk track

Compliment plus the gap — and be upfront that they already have a site:

> "You've already got a site and it looks decent. The problem is the quote path. Your hero
> is a slogan, and 'Get in Touch' drops people at the very bottom past a wall of text
> before they can ask for anything. Your Meta ads still send people into Messenger instead
> of to the site. I rebuilt it so 'get a free quote' is the first thing you see and it
> follows you down the page, added a gallery of your stamped work and gates, a financing
> payment slider, and a full Spanish version since all your ads are in Spanish. Same
> $350 plus $40/month. Here's the link — tell me what to change."

Reach them via Facebook `/concrete.diaz.ep`, Instagram `@concrete.diaz`, WhatsApp
(915) 242-3657, or a call to the same number.
