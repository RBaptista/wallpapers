# wallpapers

Wallpapers for [RBaptista/dotfiles](https://github.com/RBaptista/dotfiles), one folder per theme
(`cyan/`, `red/`, `mono/`, `purple/`, `amber/`, `green/`, `pink/`). The dotfiles' `install.sh` clones this repo to `~/Pictures/wallpapers` with
`--depth 1`, and `set-theme.sh <name>` points hyprpaper and hyprlock at the matching folder.

Adding a theme: a new folder here, plus `theme/themes/<name>` in the dotfiles.
