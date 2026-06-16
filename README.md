# Monkey Radio

A GitHub Pages site (Jekyll + Hydejack-PRO theme) for **Monkey Radio** — album
reviews from the old station, the station's story, and a live stream.

## Run it locally

System Ruby on macOS is too old. Use the Homebrew Ruby (3.4.x) and set a UTF-8
locale, or the theme's SCSS fails to compile (`Invalid US-ASCII character`).
Always export these first:

```bash
export PATH="/opt/homebrew/opt/ruby/bin:$PATH"
export LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
bundle install                 # first time only
```

### Everyday preview (recommended)

Fast rebuilds, everything works (logo, colors, content). **Search is off** —
that's by design in development.

```bash
bundle exec jekyll serve       # then open http://localhost:4000
```

### Production preview (to test search)

Search only builds with `JEKYLL_ENV=production`. In production the `github-pages`
plugin also needs a repo name; locally there's no GitHub remote yet, so pass a
placeholder and force an empty baseurl (otherwise assets like the logo 404):

```bash
JEKYLL_ENV=production PAGES_REPO_NWO="your-username/monkey_radio_reborn" \
  bundle exec jekyll serve --baseurl ""
```

Once the site is pushed to GitHub, the real repo supplies the URL automatically —
you won't need `PAGES_REPO_NWO` or `--baseurl ""` then.

> Note: a `_config.yml` change needs a server restart (Jekyll's `--watch`
> ignores it). Content/page/SCSS edits hot-reload fine.

## Where things live

| What | Where |
| --- | --- |
| Site config, menu, branding | `_config.yml` |
| Station bio / about text | `_data/authors.yml` (`author1`) |
| Minimal landing page | `index.md` |
| Detailed "Home" page | `home.md` (`/home/`) |
| Reviews index page | `_featured_categories/reviews.md` (`/blog/reviews/`) |
| Album reviews (one per file) | `_posts/YYYY-MM-DD-<slug>.md`, with `category: reviews` |

## Remaining cleanup

The site is live (https://monkeyrad.io). A few placeholders are still around:

- The `author` email in `_config.yml` / `_data/authors.yml` is still
  `you@example.com` (used by the RSS feed). Set a real address if you want one.
- Placeholder art: the logo (`assets/logo/ghost_monkey_dj.png`),
  `assets/img/sidebar-bg.jpg`, and the accent/theme colors in `_config.yml`.
- Favicon + PWA icons in `assets/icons/` are generated from `assets/logo/mic.png`
  via `sips`. To regenerate after changing the source image:
  `sips -z <px> <px> assets/logo/mic.png --out assets/icons/icon-<px>x<px>.png`
  (sizes: 16/32 for favicons, 72–512 for PWA, 180 for apple-touch).
- The hidden `_projects/rebuilding-a-radio.md` deep dive (`published: false`) is a
  stub — write it up and delete the flag when ready.

The `hydejack-pro-9.2.1/` folder is the bundled theme docs/starter kits — kept
for reference, excluded from the build and from git. Delete it when you no
longer need it.
