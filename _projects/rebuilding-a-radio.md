---
layout: project
title: "Rebuilding a Radio"
order: 5
description: >
  Turning the recovered tracks back into a station — the streaming setup, the
  playlist, and getting Monkey Radio back on the air.
# TODO (art): replace the stub image with real artwork for this page.
image: /assets/img/deep_dives/album_screenshot.png
sitemap: false
# Hidden for now — drops out of the Deep Dives grid and builds no page.
# Still a stub; write the page, then delete the line below to publish it.
published: true
---


With about 95% of the known tracks acquired, a new challenge presented itself: while providing a “shopping list” was easy enough, legitimately (that is, legally) providing people access to that content was another matter.  When Monkey Radio ran in the early 00s, the internet was young and the rules around Internet Radio still in flux.

In fact, as was noted in [the history lesson](/projects/history-lesson/), the legality of sharing this material was a recurring challenge when running the old station.  The RIAA was pushing back, and the laws changing regularly (and sometimes retroactively).

Today, the landscape has firmed dramatically.

## PROs and Cons

If you want to run an internet radio station with typical music today, you need licenses from multiple Performance Rights Organizations (PROs):

- ASCAP (American Society of Composers, Authors and Publishers): Covers a major catalog.
- BMI (Broadcast Music, Inc.): Covers another major catalog.
- SESAC (Society of European Stage Authors and Composers): A smaller, invitation-based PRO.
- GMR (Global Music Rights): Focuses on a smaller, high-profile catalog.

Webcasters may need more, and others may be required for other countries (e.g. PRS).

If you intend to host it yourself, you'll also need a server (or compute), and bandwidth.  That said, the licenses alone are _huge_ costs (in the thousands of dollars per year), and some do not issue to individuals.  This means that to start up a free radio station, you'd need to create and manage a business to even purchase said licenses.

## Administrivia

Furthermore, the DMCA has rules about what you can play when.

Per [US Copyright Code](https://www.govinfo.gov/content/pkg/USCODE-2011-title17/html/USCODE-2011-title17.htm) there are some rules you have to adhere to when broadcasting as well.

The big one is the **sound recording performance complement**, a cap on how much of any one artist or album you can play in a rolling three-hour window on a single channel. Within any **3 hours**, you may not play:

- **More than 3 songs from a single album** ...and no more than **2 of them back-to-back**.
- **More than 4 songs by the same artist**, or **4 songs from any one box set or compilation**, and no more than **3 of them back-to-back**.

In short: spread it out. You can't sit on one artist or spin a whole record straight through. The law wants a *radio station*, not an on-demand jukebox (the worry being that listeners would tape a predictable stream instead of buying the music).

A few related rules ride along with it:

- **No advance playlists.** You can't publish or announce in advance which songs are coming up, or when.
- **No song-skipping promises.** The service can't be built around letting listeners cue up specific tracks on demand.
- **Identify the track.** Title, album, and featured artist generally have to be displayed during the performance where technically feasible.

Together these are what separate a "non-interactive" webcast (the kind a statutory license covers) from an interactive, on-demand service (which needs to be negotiated directly with the rights holders).

All of this lines up to a serious set of hurdles if trying to replicate the good old days.

## Not-So-Pirate-Radio

The solution: a platform. Live365 provides blanket licenses all rolled into a subscription fee that is dramatically cheaper than purchasing licenses individually. Additionally, their AutoDJ automatically conforms to the rules about albums and tracks; I simply needed to purchase the appropriate license and upload tracks.

### The Catch

Of course, this required those tracks to be correctly managed.  My library is almost entirely FLAC, and high-bitrate whenever possible.  For my tier, Live365 requires all files to be **MP3**, encoded to a fairly specific recipe:

- **Bitrate:** between **32 and 320 kbps**, with the ceiling set by your package.
- **Sample rate:** **44.1 kHz**.
- **Channel mode:** **Joint Stereo**.
- **Bitrate mode:** **constant (CBR)** — *not* variable (VBR).

So every FLAC had to be transcoded down to a conforming MP3. (Going lossless to lossy is a one-way trip, but a streaming platform was always going to be lossy anyway). I set the bitrate to 192kbps--the highpoint of the station when it ran.

### Tag, You're It

The audio is only half the job; Live365 leans on each file's **ID3 tags** to drive the stream. At minimum every track needs clean **Title**, **Artist**, and **Album** fields, since that's what gets pushed out as now-playing metadata and what the AutoDJ uses to enforce the artist/album spacing rules above. Garbage in, garbage out: a missing or mislabeled artist tag doesn't just look sloppy on the listener's screen, it can let the rotation drift out of compliance. Album art embedded in the tags carries through to the player as well.

So my workflow became:

>  1. Acquire tracks through digital storefronts, or digitize using EAC (or more involved methods, for vinyl).
>  2. Add the files separately to a Monkey Radio Archive as well as my personal library.
>  3. Re-encode all files to Live365 specifications using ffmpeg.
>  4. Run Musicbrainz Picard on the resulting files to clean any metadata for Live365.

## The Result: A Station Reborn

The Monkey Radio Archive is my best attempt to make the station available again. It's unofficial, and built entirely using historical records and first-hand accounts; while I can't guarantee it is perfectly accurate (and am quite confident there are tracks it is missing) it is a best effort, and I continue to seek to improve it with new information or access to missing tracks. I hope you enjoy listening to a fan-recreation of the old sound!

If you know of tracks it is missing (or have information for the history books) reach out!