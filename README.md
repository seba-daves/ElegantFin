# ElegantFin — SebaEdit

A personal flavour of [ElegantFin](https://github.com/lscambo13/ElegantFin) by [lscambo13](https://github.com/lscambo13), a Jellyfin theme inspired by Jellyseerr. All credit for the original theme goes to the upstream author. For screenshots, the full feature list and support, see the [upstream repository](https://github.com/lscambo13/ElegantFin).

## What's different in this fork

- **Jellyfin 12 preliminary fixes:** a separate `jf12` build of the theme and of the Media Bar add-on.
- **Media Bar plugin tweaks** for both Jellyfin 12 and older versions.
- **Custom media covers:** extra `christmas` and `podcasts` library covers.
- **Self-hosted fonts:** fonts are bundled in `fonts/` instead of loaded from Google Fonts.
- **Slimmer repository:** only the files needed to use the theme are kept, at the repository root (`assets/`, `fonts/`) instead of under `Theme/`.

Based on ElegantFin **v26.09.05**, plus upstream fixes merged since then (latest: Tizen fixes, [#321](https://github.com/lscambo13/ElegantFin/pull/321)).

## Installation

In Jellyfin, go to **Dashboard → Branding → Custom CSS code**, paste the snippet for your Jellyfin version, and save. Refresh the page (or clear the cache) to see the changes.

The `./` paths below are resolved relative to your Jellyfin web client. To use them, copy this repository's files there. Otherwise, replace `./` with `https://cdn.jsdelivr.net/gh/seba-daves/ElegantFin@main/` to load the files straight from this repository.

### Jellyfin 12 (preliminary)

```css
/* Media Bar support */
@import url("./assets/add-ons/media-bar-plugin-support-v26.09.05.jf12-SebaEdit.css");
/* Main theme */
@import url("./ElegantFin-theme-v26.09.05.jf12-SebaEdit.css");
/* Custom media covers */
@import url("./assets/add-ons/custom-media-covers-v26.09.05-SebaEdit.css");
```

### Jellyfin < 12

```css
/* Media Bar support */
@import url("./assets/add-ons/media-bar-plugin-support-v26.09.05.css");
/* Main theme */
@import url("./ElegantFin-theme-v26.09.05-SebaEdit.css");
/* Custom media covers */
@import url("./assets/add-ons/custom-media-covers-v26.09.05-SebaEdit.css");
```

The Media Bar and custom covers lines are optional. Remove them if you don't use those features.

## Files

| File | Use |
| --- | --- |
| `ElegantFin-theme-v26.09.05-SebaEdit.css` | Main theme, Jellyfin < 12 |
| `ElegantFin-theme-v26.09.05.jf12-SebaEdit.css` | Main theme, Jellyfin 12 |
| `assets/add-ons/media-bar-plugin-support-v26.09.05.css` | Media Bar support, Jellyfin < 12 |
| `assets/add-ons/media-bar-plugin-support-v26.09.05.jf12-SebaEdit.css` | Media Bar support, Jellyfin 12 |
| `assets/add-ons/custom-media-covers-v26.09.05-SebaEdit.css` | Custom library covers (images in `assets/img/library-covers/`) |
| `fonts/` | Self-hosted fonts used by the theme |

## Keeping up with upstream

Upstream changes are merged into this fork periodically. Upstream's `Theme/ElegantFin-theme-nightly.css` corresponds to `ElegantFin-theme-v26.09.05-SebaEdit.css` here. Relevant fixes are also applied to the `jf12` files.

## License

See [LICENSE](LICENSE). The original theme is © [lscambo13](https://github.com/lscambo13/ElegantFin).
