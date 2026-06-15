---
layout: page
title: "Chasing the Monkey: Rebuilding Internet History"
permalink: /chasing-the-monkey/
description: >
  The hunt to figure out what Monkey Radio actually played — and to rebuild it
  from forum playlists, old CDs, and a lot of detective work.
---

Rebuilding a slice of internet history, one track at a time.
{:.lead}

[↓ Jump to the Deep Dives](#deep-dives){:.btn.btn-primary}

Back in 1999, an internet radio station called **Monkey Radio** went live — chillout, down-tempo,
trip-hop, and smooth jazz, an eclectic mix of artists you'd be unlikely to hear
on traditional radio. Thanks to it, I discovered artists like DJ Krush, Kruder &
Dorfmeister, and A.P.E. It became the sound of a productive workday.

## The challenge
The problem is, it's hard to say what was actually *on* Monkey Radio given we lack the raw playlist data. 
There's a hand-built playlist document from 2002 that was posted on a forum, and other folks
have shared Spotify and YouTube playlists that fill out the picture with more
recent content.

Armed with a Plex server, a healthy portion of these tracks on old CDs, and a deep
desire to buy the rest and replicate the station for my own entertainment, I started hunting. 
That turned out to be harder than it sounds: the 2002 playlist is full of errors —
swapped artists and track names, misspellings, duplicates — and lists no album
names. It also only runs through 2002, so other (less complete) lists have to
fill the gaps with newer artists like Hird.

## Rebuilding the rotation
So I set out to use a mix of scripts, AI, and old-fashioned web sleuthing to
consolidate as many tracks as possible into as few albums as possible — many of
them collected on compilations and remix albums. I'm sharing the results in case
anyone else has the same impossible dream:

[**The consolidated album spreadsheet**](https://docs.google.com/spreadsheets/d/1boLv9FFnjjzpS9O0828yRW1H3c6VIxN624_I4zYVXBI){:.heading.flip-title}

It lists my best guess at the album, artist, and tracks for each entry, along
with the source list it came from. For anything with 3+ tracks I've added a
place to buy it in lossless (Bandcamp, Qobuz, Juno, or just old CDs). Links rot
fast, so YMMV.

A few notes on the data:

* **Many tracks are remixes.** I've removed a lot of cross-collection duplicates,
  which may have accidentally culled some original versions. There's heavy
  cross-pollination, so most are still present somewhere on the artists' albums.
  I kept tracks that were explicitly different versions — but if you're confident
  something shouldn't have been dropped, let me know...
* **Some only exist on old CDs.** The internet was young, and many of these
  artists were obscure enough to fall through the digital-storefront cracks. At
  least one track only exists on a 12" vinyl, best I can tell.
* **Expect errors.** I've checked and reviewed by hand and with automation, but
  any time scripts or LLMs are involved, issues are likely.

Thanks to the folks at the [Monkey Radio fan-site on Facebook](https://www.facebook.com/MonkeyRadio.org/)
for collecting the sources I started from. If I missed any big albums or
consolidations, let me know — I just wanted to share a bit of internet history.

---

## Deep dives {#deep-dives}
Longer write-ups on individual aspects of the rebuild. (More to come.)

<!-- Grid of image-cards linking to the `_projects` collection (pages that live
     outside the blog feed). Ordered by each page's `order:` front matter. -->
<div class="columns columns-break">
{% assign deep_dives = site.projects | sort: 'order' %}
{% for project in deep_dives %}
  <div class="column column-1-2">
    {% include pro/project-card.html project=project %}
  </div>
{% endfor %}
</div>
