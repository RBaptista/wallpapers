# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

An image-only repo of wallpapers for [RBaptista/dotfiles](https://github.com/RBaptista/dotfiles). There is no code, build, lint, or tests here. Each top-level folder is a theme (`cyan/`, `red/`); the folder name must match a theme in the dotfiles (`theme/themes/<name>`).

How it's consumed (lives in the dotfiles, not here):
- `install.sh` clones this repo to `~/Pictures/wallpapers` with `--depth 1`.
- `set-theme.sh <name>` points the wallpaper rotation (`wallpaperd.sh`, awww), hyprlock and the SDDM login screen at `~/Pictures/wallpapers/<name>/`. Each theme file in the dotfiles (`theme/themes/<name>`) names a `lock=` and a `login=` image in its folder: never move or rename those two without updating that file.

So renaming or removing a theme folder breaks the dotfiles theme of the same name, and adding a theme needs both a folder here and `theme/themes/<name>` in the dotfiles.

## "Commit and push" workflow

The user's flow is to drop downloaded images into a theme folder, then ask Claude to "commit and push". When asked, do all of this without further prompting:

1. Find new images with `git status --porcelain` (untracked or added files in theme folders).
2. Open each image with the Read tool to see what it shows, and rename it (`mv`) to a descriptive kebab-case name. Keep the original extension, drop source IDs and resolution suffixes, and don't reuse a name that already exists in that folder.
3. If an image's main colour clearly doesn't match its folder, don't move it. List it in the summary so the user can decide.
4. Commit with a conventional message (e.g. `feat: add new cyan and red wallpapers`), then `git push` to `origin main`.
5. Report the old → new names.

## Conventions

- Files are named with descriptive kebab-case names of what the image shows (e.g. `crimson-moon-clouds.png`, `turquoise-lake-waterfall.png`), not source IDs.
- An image belongs in the folder whose color matches its dominant palette, regardless of its name (see commit `3609060`, which moved `red-portal-machinery.png` from `cyan/` to `red/`).
- Both `.png` and `.jpg` are in use.
- Commit messages use conventional-commit prefixes (`feat:`, `fix:`).

## Theme moods

Several themes share a hue, so a folder is defined by mood as well as colour. When an image could fit two folders, the mood decides. Decided on 2026-11-01, when pink/purple and the blues were split this way.

- `pink/` (Dracula): loud. Neon, synthwave, cyberpunk, magenta glow, saturated pink sunsets.
- `purple/` (Catppuccin): quiet twilight. Dusk, mist, night forests, fantasy, calm violet skies.
- `cyan/` (Tokyo Night, the default): electric. Sci-fi, tech, HUDs, neon, night auroras, underwater glow.
- `blue/` (Kanagawa): indigo night Japan. Torii, temples, rainy neon streets, moonlit cities.
- `frost/` (Nord): bright snow and ice. Daylight, white, overcast, glaciers. Night auroras go to cyan; frost keeps only `night-aurora-tundra` (its login image).
- `amber/` (Gruvbox): warm gold and orange. Sunsets, deserts, golden light, fire.
- `green/` (Everforest): forests, ferns, lush nature, terminal/matrix green.
- `red/` (Rosé Pine palette, true-red accent): crimson. Blood moons, red shrines, fire.
- `mono/`: black and white, near-grey, a single small colour accent at most.

An image goes in exactly one folder.

## Adding wallpapers from Wallhaven

How the 2026-10-31 top-up was done; reuse it.

1. Search the API with curl (`https://wallhaven.cc/api/v1/search`): `categories=110` (general + anime), `purity=100` (SFW), `atleast=1920x1080`, `ratios=16x9,16x10`, `sorting=toplist`, `topRange=1y` (the default 1M returns very few), `colors=<hex>` from Wallhaven's fixed colour list plus a mood word in `q` (`snow`, `dusk`, `fog`, `japan night`). Skip files over ~9 MB. Use curl rather than a script with a spoofed user agent: the API rejects Python's default one.
2. Download the small thumbnails, build numbered contact sheets with `montage`, look at them, and pick by mood (above), not only by colour.
3. Before adding, compare every pick against the whole repo with a perceptual hash (9x8 grayscale dHash; flag distance ≤ 12). Toplist results overlap heavily with what's already here. Dark or flat images give false matches, so confirm flagged pairs by eye.
4. Name and commit as in the workflow above.

Aim for roughly 32–35 images per theme so "random theme at login" doesn't repeat images too soon; `cyan/` is the default and is bigger (~84).
