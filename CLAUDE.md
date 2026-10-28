# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

An image-only repo of wallpapers for [RBaptista/dotfiles](https://github.com/RBaptista/dotfiles). There is no code, build, lint, or tests here. Each top-level folder is a theme (`cyan/`, `red/`); the folder name must match a theme in the dotfiles (`theme/themes/<name>`).

How it's consumed (lives in the dotfiles, not here):
- `install.sh` clones this repo to `~/Pictures/wallpapers` with `--depth 1`.
- `set-theme.sh <name>` points hyprpaper and hyprlock at `~/Pictures/wallpapers/<name>/`.

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
