The personal website of Jeff Tellew.

Accessible at jefftellew.github.io (surprise surprise) or by [clicking here](https://jefftellew.github.io "jefftellew.github.io").

Includes basic information about me, my education and professional experience, and programming projects I've worked on.

## Running it locally

It's a static site, so opening `index.html` in a browser mostly works. To get paths behaving the way they do in production:

```
python -m http.server
```

Then visit http://localhost:8000.

## Layout

```
index.html          the whole site -- it's one page
css/style.css       my styles; the rest of css/ is Bootstrap
js/                 Bootstrap bundle and jQuery
res/img/            project screenshots and photos
res/icons/          section and button icons
res/downloads/      resume
```

## Dependencies

Bootstrap 4.4.1 and jQuery 3.7.1 (slim) are vendored into `css/` and `js/` rather than loaded from a CDN. There's no package manager here, so updating either one means dropping in the new files by hand and updating the `<script>`/`<link>` tags in `index.html`. The Bootstrap *bundle* includes Popper, so don't add a separate Popper tag.

## A note on assets

GitHub Pages serves everything in this repo, and the repo has to stay clonable, so large binaries don't get committed:

- Downloadable builds go on a [GitHub release](https://github.com/jefftellew/prometheus/releases) of the project's own repo, and the site links to the release asset. The Prometheus `.jar` is 71 MB and used to live here; it doesn't anymore.
- Animations ship as an `.mp4` with a `poster` image, not a `.gif`. The UltraTracker clip went from a 5 MB gif to a 580 KB video that way.

## Credits

Header animation by [Beeple](https://www.beeple-crap.com/). Icons from [svgrepo.com](https://www.svgrepo.com/) or their respective official websites.
