# Simple Compile

**Version 1.0** — a stable, released app.

A one-page, no-editing version of Minutes: open a CSV, get readable minutes back. No Setup,
no Capture, no Song List to fix up, no saved project — open a file, read the output, copy or
share it, done.

One HTML file, plus the same shared tunebook library and utilities the rest of the Suite
uses. Nothing to install, no server, no build step.

## Part of the Sing Loud Suite

| App | What it does | Status |
|---|---|---|
| [**Minutes**](https://github.com/singlouddotorg/minutes) | Log a singing as it happens, then turn that log into publishable minutes — with full editing. | Beta |
| [**Tunebooks**](https://github.com/singlouddotorg/tunebooks) | Curate the shared tunebook data — editions, page indexes, Level 3 scholarly files. | Beta |
| [**Simple Minutes**](https://github.com/singlouddotorg/Simple-Minutes) | A phone-sized logger: page numbers only, no names. Its files import straight into Minutes and Simple Compile. | 1.0 release |
| **Simple Compile** | This app. | 1.0 release |
| [**Simple Totals**](https://github.com/singlouddotorg/Simple-Totals) | Combines many finished singings into one master record and set of totals. | New (0.1) |
| [**Tunebook Registry**](https://github.com/singlouddotorg/tunebook-registry) | The published tunebook data the others read. | 1.0 release |

## What it is for

The everyday case: a singing already logged in Simple Minutes (or a Master CSV from the full
Minutes app), and someone just wants readable minutes out of it — to paste into an email, a
website post, or the SHMHA Minutes Book submission — without opening the full editor at all.
It shares Minutes' own generation engine exactly (the same import parser, the same Minutes
Maker/SHMHA/Simple List builders), so anything Simple Compile produces will always read the
same as the full app would produce from the same file. What it leaves out is everything
*around* that: no Song List to fix up, no book-source management, no per-day locations, no
name-variant merging, no saved project to keep track of. If a file genuinely needs
correcting — a mistyped page, a name to fix — open it in the full [Minutes](https://github.com/singlouddotorg/minutes)
app instead; Simple Compile's own "Export .csv" isn't offered here on purpose (see
"Copy and Share" below), but the file it read is untouched and opens there just as it is.

Leaderless files — Simple Minutes' everyday output — are the case this app is built around:
importing one is detected automatically, and the minutes read as prose about *what was sung*
rather than "the leader" repeated once per song. Nothing has to be configured for that to
happen, though the checkbox that controls it is right there if a file needs it set by hand.

## Using it

1. Open `index.html` and drop in a CSV — a Simple Minutes export, or a Master CSV from
   Minutes.
2. Pick the type of output: **Minutes Maker** (narrative prose), **SHMHA Minutes Book
   Submission** (their fixed format), or **Simple List** (a terse scan list).
3. Adjust whichever options matter for that output — they're the same settings the full app
   offers on its own Export tab, just gathered onto this one page.
4. **Copy to clipboard**, or tap **Share** to hand the text straight to Mail, Messages, Notes,
   or whatever the device offers (hidden automatically on a browser that doesn't support
   sharing — Copy always works either way).

## Copy and Share, not Download

Every other app in this Suite writes files. Simple Compile deliberately doesn't: the point
was always "copy/paste/email," not producing another file to manage, so there's no download
grid of formats here. Copy and Share both hand off the exact text shown in the preview,
whatever output type and options are currently selected.

## Nothing is saved

Simple Compile keeps no project between visits and writes nothing to browser storage in
either direction. Opening a second file replaces the first outright (with a confirmation if
the first one had real content) — refreshing the page starts completely clean. If a singing
needs revisiting later, keep the original CSV; Simple Compile is a one-way read of it, not a
place to store it.

## Nothing is uploaded

No file, and no part of the minutes it generates, is ever sent anywhere. Everything happens
in the browser; Copy and Share hand text to the operating system, not to a server.

## Where the songbook data comes from

`tunebook-library.js` ships bundled right beside `index.html`, exactly like every other app
in this Suite — read strictly as data, never executed as code.
