# QuizMaster — landing page

A one-page, responsive landing page for QuizMaster, a timed quiz app with
a live countdown, auto-submit, and server-side scoring.

## How to run it

No build step — it's plain HTML/CSS.

1. Download or clone this repo.
2. Open `index.html` directly in a browser.
3. Visit the page (or the local server's URL) and resize the window / open
   dev tools' device toolbar to check the mobile layout.

## Structure

```
index.html   — page markup and content
style.css    — all styling, mobile-first with a single breakpoint set
```

## Decisions worth noting

- **Content is real, not placeholder.** The copy describes an actual app
  concept (role-based sign-in, server-side scoring, countdown auto-submit,
  leaderboard) rather than filler text.
- **No raster images.** The hero visual and small icons are inline SVG, so
  there's nothing to overflow the viewport and nothing to fail to load —
  they scale with `max-width: 100%` like any other image would.
- **Breakpoints:** the layout is single-column by default and switches to
  a two-column hero/features grid at `640px`–`860px` depending on the
  section. Tested with no horizontal scroll at a 375px viewport width.
- **Two accent colors (amber + teal)** instead of one, so the page doesn't
  read as a generic dark-mode template — amber ties to the timer/urgency
  idea, teal to "correct answer."
- **Answer-bubble motif** (A/B/C/D circles) is used for the feature list
  and the hero SVG because the subject matter — a quiz app — is literally
  about multiple-choice bubbles. The 1–4 numbered list is used only for
  "How it works," because that content is an actual sequence.
