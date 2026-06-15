---
layout: project
title: "Efficiency: Album Consolidation"
order: 2
description: >
  Collapsing 1600+ scattered tracks into as few albums as possible — compilations,
  remix albums, and the tier system for buying it all.
# TODO (art): replace the stub image with real artwork for this page.
image: /assets/album_covers/cold-krush-cuts-4-main.jpg
sitemap: false
---

As detailed in the [Sources Deep Dive](/_projects/the-sources.md), I had put together multiple lists of tracks.  Unfortunately, many of these were just that -- artist and track names (often misspelled or wrong).  I used a combination of python scripts and LLMs alongside the Musicbrainz API to fuzzy-match, swap, and otherwise munge track names to look for normalized track names, then manually reviewed the resulting reports.  Then...I needed to look for albums.

Searching by hand was quickly infeasible.  In particular, it wasn't sufficient to locate _an_ album for the track; with more than 1600 entries, that would get (more) expensive very quickly.  Skimming the list and searching by hand, many artists only had one or two tracks from an album on the list.

An easy assumption might have been that the tracks were pirated--but Underwood had vocally criticized people stealing from artists with tools like Napster. I theorized that many of the tracks were instead from a 90s staple: compilations.

## Compilations

Anyone who watched late-night TV in the 90s no doubt remembers exactly what I'm referring to -- while digital storefronts were not yet common, collections of genre music could be bought from CD stores and infomercials alike. Here, I tapped a combination of LLMs (claude and chatgpt), the discogs API, and the musicbrainz API to look for popular collections of triphop, downtemp, and acid jazz, and compare those to my track list.

The result: Pure gold.

![Hed Candi: Winter Chill](/assets/album_covers/hed_candi_winter_chill.jpg){:style="float:left;width:24rem;margin:0.25rem 1.5rem 1rem 0;"}
_Cold Crush Cuts_ contained 32 Monkey Radio tracks. _The K&D Sessions_, a legendary mix album, included 17. _Hed Kandi: Winter Chill_ provided 18 (with a caveat, see below!). Many of these albums come with impressive names (Ninja Cuts: Funkungfusion, is a personal favorite). Given that we have Underwood's word that he purchased most/all of this music, this went a long way to answering _how_ he acquired this _particular_ set of tracks.

Not all compilations were just collections of otherwise-available music, either: some feature tracks that are nowhere on the artists' normal catalog of albums. So even for artists that one should buy whole-cloth (Thievery Corporation, etc.) dipping into compilations, singles, and EPs is required.

## Approach

At this point, I operated in multiple passes:

- I used the discogs API to get a list of albums associated with each track on my list.
- I also iterated through popular compilations of the era and looked for tracks matching my list.
- I iterated through each resulting album, checked the list for items in my playlist, then prioritized according to the albums with the highest track counts.
- I then assigned albums to each entry.

(To be completely accurate, I went through a wide variety of other, less effective approaches as well--this gets the gist across though).

## Result

The tracks have been associated with albums, then sorted according to the number of tracks on that album, allowing me to acquire the whole list (comparatively) efficiently. This list is not without problems, however: due to errors in discogs or musicbrainz, coincidences in naming, or LLM error, removing inaccuracies has been a very manual affair. 

The final passes involve purchasing the ablums, and extracting the specific tracks to archive them for upload to the station--by that point, the rubber is meeting the road. This resulted in learning a lot about the artists that I've come to love (and about the music industry in general). But that's a story for another Deep Dive...