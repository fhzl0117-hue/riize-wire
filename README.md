# RIIZE Wire

An independent, unofficial English-language fan hub for RIIZE/BRIIZE — news translation, release reviews, official-only video curation, a live tour countdown, and a fan quiz, built to run on Google AdSense.

**Not affiliated with, endorsed by, or sponsored by SM Entertainment or the members of RIIZE.**

## What's in this repo

This is a single static page — `index.html` — with everything (HTML, CSS, JS) inlined. No build step, no dependencies, no backend. It's meant to be served as-is by GitHub Pages. This repo follows the same template as [Bangtan Wire](https://fhzl0117-hue.github.io/bangtan-wire/), [Blackpink Wire](https://fhzl0117-hue.github.io/blackpink-wire/), [Stray Kids Wire](https://fhzl0117-hue.github.io/stray-kids-wire/), [aespa Wire](https://fhzl0117-hue.github.io/aespa-wire/), [ENHYPEN Wire](https://fhzl0117-hue.github.io/enhypen-wire/), [SEVENTEEN Wire](https://fhzl0117-hue.github.io/seventeen-wire/), [TWICE Wire](https://fhzl0117-hue.github.io/twice-wire/), [LE SSERAFIM Wire](https://fhzl0117-hue.github.io/lesserafim-wire/), [TXT Wire](https://fhzl0117-hue.github.io/txt-wire/), and [(G)I-DLE Wire](https://fhzl0117-hue.github.io/gidle-wire/) — part of the "Wire" series, one dedicated site per artist.

The page is organized into six "desks," each mapped to a content pillar:

| Desk | Section id | What it does |
|---|---|---|
| 01 · News | `#news` | Translated & summarized news dispatches, each linking to its original source |
| 02 · Review | `#reviews` | Album / track reviews, text only |
| 03 · Screening Room | `#screening` | Official YouTube embeds only — never re-uploaded video |
| 04 · Signal | `#signal` | A live timer that counts down to confirmed future tour dates, or counts up ("time since") for past ones — auto-converted to the visitor's local timezone |
| 05 · Quiz | `#quiz` | A lightweight interactive quiz, no backend, no data collection |
| 06 · Market | `#market` | Links to official stores (affiliate links go here) |

## A note on accuracy: the lineup and fandom name

RIIZE debuted in September 2023 as a seven-member group. Member Seunghan left in October 2024 amid a lineup controversy and now performs independently as XngHan; RIIZE has continued as a six-member group (Shotaro, Eunseok, Sungchan, Wonbin, Sohee, Anton) since. The official fandom name was also changed to "BRIIZE" after an earlier name drew criticism from fans. Keep both facts in mind when writing new copy — don't refer to the group as seven members, and use "BRIIZE" for the fandom.

## A note on accuracy: the Riizing Loud World Tour

As of this build (August 2026), the Riizing Loud World Tour (behind debut album *Odyssey*) ran from July 2025 through its Seoul finale in March 2026, including a record-setting three-night Tokyo Dome run in February 2026 (the fastest-ever K-pop boy group entry into the venue, per allkpop). No new world tour had been announced at time of writing. Do not add new tour dates to the Signal desk unless confirmed by SM Entertainment, Soompi, or another reputable outlet — don't assume the II era will get its own tour without a source.

## manifest.json — K-Wire Network auto-discovery

This repo carries a `manifest.json` at its root so it's automatically picked up by [K-Wire Network](https://fhzl0117-hue.github.io/), the directory hub for the whole "Wire" series. No manual edit to the hub repo is needed — its page fetches this file on every visit and lists this site automatically.

## Updating content

Everything is plain HTML — open `index.html` in any editor and look for the section with the matching `id` (e.g. `<section ... id="news">`) to update copy. There's no CMS yet; each dispatch, review, or signal-desk date is a hand-edited block. See the comments inside the `<script>` tag at the bottom for how the quiz and countdown/elapsed timers work if you need to change their logic — the Signal desk timer auto-detects whether a `data-target` date is in the future (shows "time left") or the past (shows "time since"), so it works either way without further edits.

**Before adding new dates or news items,** verify the underlying facts against a real source and keep the "Read the original source" link pointing at it — that link is what keeps this page compliant with content policies (Google AdSense does not allow re-publishing copyrighted material, and this page's whole design is built around linking out and summarizing instead of reposting).

**Before adding any new YouTube embed,** verify it against the official channel using the oEmbed check: fetch `https://www.youtube.com/oembed?url=https://www.youtube.com/watch?v=<ID>&format=json` and confirm `author_name` matches "SMTOWN" on channel `@SMTOWN` (RIIZE, like other SM artists, publishes MVs through the shared SMTOWN channel rather than a group-specific one) — a search result titled "Official MV" is not proof by itself. Both embeds in this initial build ("Do your dance" and "Fly Up") were verified this way.

## License / ownership

Internal company project. Not licensed for redistribution outside the team without checking with whoever owns this repo.
