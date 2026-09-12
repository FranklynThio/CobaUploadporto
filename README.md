# Franklyn Thioatmadjaya — Portfolio

Personal portfolio site. Live at **https://franklyn-porto.vercel.app/**

Single-page, hand-written HTML/CSS/JS — no framework, no build step. Open `index.html` and it runs.

## Stack

- Vanilla HTML, CSS and JavaScript
- Google Fonts: Sora, IBM Plex Sans, IBM Plex Mono
- GitHub REST API for the live repository feed
- Deployed as a static site on Vercel

## Structure

```
index.html   the whole site — markup, styles and script
assets/      project screenshots, portrait, CV
```

## The GitHub section

The "Straight from GitHub" section ships with an embedded snapshot of the public
repositories so the page is complete before any network call, then fetches
`api.github.com/users/FranklynThio/repos` on load and replaces the list with live
data. If the request is blocked or rate-limited, the snapshot stays and the status
label reads "Snapshot" instead of "Live".

## Editing

Everything lives in `index.html`:

- design tokens — the `:root` block at the top of `<style>`
- experience entries — the `<section id="experience">` timeline
- projects — the `<article class="proj">` cards; screenshot filenames are
  listed in the `galleries` object in the script
- skills — the `<section id="skills">` columns and the `items` array that feeds
  the scrolling tech strip

Pushing to `main` triggers a Vercel deployment.
