---
layout: project
title: The Sources
# `order` controls the position in the grid on /chasing-the-monkey/.
order: 1
description: >
  Where the track lists came from — the 2002 forum playlist, the Wayback Machine
  and the Spotify/YouTube/Discogs lists that fill in the gaps.

image: /assets/img/deep_dives/sources.png
sitemap: false
---

The trick to recreating the old Monkey Radio feeling is in finding the music.

The problem: this wasn't something that was publicly documented in a meaningful way.  Those of us that listened certainly remember impactful tracks, but the station featured a staggering array of music in the genre, much of which you'd _only hear there_.

I'm not the first to have done work in the space--and everyting I did was built on their efforts.  The first place I looked was a fan [Facebook Group](https://www.facebook.com/MonkeyRadio.org/). It had links to a lot of useful starting points I could work from.

When attempting to reconstruct the station, there's one authoritative place to start: 2002.

## 2002 - An authoritative snapshot
![2002 Playlist](/assets/img/deep_dives/2002_playlist.png)

In part due to his struggles with the RIAA and ongoing legislation around internet radio stations, the Monkey Radio creator posted a copy of his playlist in 2002.  A fan subsequently took this list and started hunting tracks on it -- the file is currently still available on google drive:

[Original 2002 list](https://docs.google.com/spreadsheets/d/1nmnS7z8AbMsRhleVO_9e7jttkFBEL3kv1j0IzFLafkA/edit?usp=sharing)

As you might notice in the image above, however, this immediately presents several serious challenges:
- The file (as is common in the era) was hand-built. Spelling and capitalization vary dramatically, artists and track names may be swapped or mispelled. Some remixes don't appear to exist at all (likely transcription errors when it was being created).
- There are a fair number of duplicates -- possibly due to being added for the original and the remix, possibly due to the originator's library being messy and/or containing extra copies (many of these tracks were featured on compilations).
- Additionally, this was 2002 -- and Monkey Radio ran througn 2013. There's a lot of music that played on the station later that just didn't exist yet.
- Finally, note that there are no album names. Only track names...


## Streaming services
The fan began putting together a YouTube playlist based on this 2002 list. That said, a much more thorough list was built by a different fan; this list was more than 470 tracks, and included a number of items that post-dated 2002:

[Youtube Playlist](https://www.youtube.com/watch?v=MpAJ0NvkbLY&list=PLa9q0QPCXV9sTSPx1G7H4JVHMXeV3LNd-)

Additionally, a separate individual (I believe the same one that runs the Monkey Radio fan facebook group) added the spotify tracks that they could find to a playlist; up until this point that is one of the largest collections of Monkey Radio tunes one can listen to at more than 750 songs: 

[Spotify Playlist](https://open.spotify.com/playlist/1plJAm2h7qXQtxkSl82DDz)

### The problem

Both of these provide good sources to intoroduce people to the style of the old station, but they had a serious handicap: they could only play music already present on their respective platforms. Given that Monkey Radio was created at a transitional period of the Internet, _many_ of the tracks are not present on either platform, having never made the transition to digital distribution.

Furthermore, while I utilized both sources, it's important to caveat that these are distinctly less official than the original 2002 playlist. Some items on those lists may not have been originallally played on the radio (I'm looking at you, K&D's "1995") even if they absolutely fit the vibe.

## On a similar note: Discogs

There is also a discogs list of Monkey Radio tunes that have been released on Vinyl. The fan-built list was referenced on the homepage of Monkey Radio late in its lifespan, and it still receives occasional updates as of 2026. It only reflects tracks that have Vinyl releases of course, but is still a resource for tracking down content belonging to the station, and Underwood's acknowledgement of it adds some authenticity to the mix:

[Discogs Vinyl List](https://www.discogs.com/lists/Monkey-Radio-on-vinyl/10125?srsltid=AfmBOooq6qoo33bQ13wAfxSLITtjHJvFGYNO7ks_rfmnszLEFGkf3yII)

## Eureka: Data from Wayback

That said, there's one more highly authoritative site: the Wayback Machine.  The Internet archive snapshots web pages periodically; I realized that on ever snapshot of every subpage on monkeyradio.org, there was an element listing "current song" (e.g. _Current song: Fluke - Bermuda_).  

Furthermore, there was also a Recent Playlist link showing the last 20 songs in the rotation until the site's revamp.  I wrote a script that would crawl through downloaded snapshots from Wayback and extract a list of songs from the relevant fields in each subpage's snapshot, then deduplicate them -- this added a nearly a hundred tracks that hadn't been present in any of the above lists!

# The Caveats

After deduplication, we now had a massive list of more than 1600 tracks.  This list comes with some caveats:

1) Some of the sources (fan lists) aren't official in any meaningful way -- if they misremember what was on the station, "bad" data will creep in.

2) In the 2002 list, the data was very hand-crafted -- meaning you had multiple copies of tracks, often slightly differently named.  Tracks would be mislabled, misattributed, or named in ways that make it difficult or impossible to confidently assign them (e.g., DJ Krush's "Interlude" -- lacking an album name, there are technically several that might fit this bill).

3) Some of these tracks are definitely not official releases; for example, one by Blioux is almost certainly a live recording from Underwood's birthday. More on that in another article.

