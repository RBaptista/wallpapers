# Themes

What each folder has to match, copied from the dotfiles (`~/dotfiles/theme/themes/<name>` and
`~/dotfiles/theme/palettes/<palette>`). If a theme changes there, update it here too.

- **accent**: the theme's highlight colour (`accent=` in the theme file).
- **bg / fg**: the palette's background and text colours. A wallpaper should sit well behind them.
- **lock / login**: the hyprlock and SDDM images. Never move or rename them without editing the theme file.
- **Wallhaven**: `colors=` values (Wallhaven only accepts its fixed list, below) and `q` words to search with.

Wallhaven's colour list: `660000 990000 cc0000 cc3333 ea4c88 993399 663399 333399 0066cc 0099cc 66cccc
77cc33 669900 336600 666600 999900 cccc33 ffff00 ffcc33 ff9900 ff6600 cc6633 996633 663300 000000 999999
cccccc ffffff 424153`.

| Theme | Palette | Accent | bg | fg | Lock | Login |
|---|---|---|---|---|---|---|
| amber | Gruvbox dark | `fe8019` | `282828` | `ebdbb2` | `ocean-sunset-storm-clouds.jpg` | `mountain-sunset-tree-silhouette.png` |
| blue | Kanagawa wave | `7e9cd8` | `1f1f28` | `dcd7ba` | `torii-starry-night.jpg` | `moon-shooting-stars-sakura.jpg` |
| cyan | Tokyo Night (default) | `00ffff` | `1a1b26` | `c0caf5` | `neon-ring-minimal.jpg` | `aurora-lake-night.jpg` |
| frost | Nord | `88c0d0` | `2e3440` | `d8dee9` | `indigo-mountain-valley.jpg` | `night-aurora-tundra.jpg` |
| green | Everforest dark | `a7c080` | `2d353b` | `d3c6aa` | `green-crescent-glow.png` | `misty-redwoods-ferns.jpg` |
| mono | Tokyo Night, text-coloured accent | `c0caf5` | `1a1b26` | `c0caf5` | `black-cat-blue-eyes.png` | `black-hole-eclipse-clouds.png` |
| pink | Dracula | `ff79c6` | `282a36` | `f8f8f2` | `pink-planet-crescent-moon.jpg` | `painted-pink-sky-mountains.jpg` |
| purple | Catppuccin Mocha | `cba6f7` | `1e1e2e` | `cdd6f4` | `mountain-sunset-city-lights.png` | `violet-palace-lake-boat.png` |
| red | Rosé Pine (true-red accent) | `e5484d` | `191724` | `e0def4` | `naruto-itachi-blood-moon.png` | `city-skyline-sunset.png` |

## amber (Gruvbox)
Warm gold and orange: sunsets, deserts, golden light, fire. Gruvbox is earthy, so muted browns and
dusty oranges fit better than neon orange. Palette yellow `fabd2f`, orange `fe8019`, red `fb4934`.
- Wallhaven: `ff9900`, `cc6633`, `ffcc33`, `996633`. q: `sunset`, `desert`, `autumn`, `golden`, `fire`.

## blue (Kanagawa)
Indigo night Japan: torii, temples, rainy neon streets, moonlit cities. Kanagawa is ink-blue with
faded, woodblock-print tones (crystal blue `7e9cd8`, wave blue `7fb4ca`, autumn red `c34043`).
- Wallhaven: `333399`, `0066cc`, `424153`. q: `japan night`, `temple`, `rain city`, `moon`.

## cyan (Tokyo Night, the default)
Electric: sci-fi, tech, HUDs, neon, night auroras, underwater glow. Pure cyan `00ffff` on deep navy,
with Tokyo Night blue `7aa2f7` and magenta `bb9af7`. Biggest folder (~84); top up only when asked.
- Wallhaven: `0099cc`, `66cccc`, `0066cc`. q: `aurora`, `cyberpunk`, `sci-fi`, `underwater`.

## frost (Nord)
Bright snow and ice: daylight, white, overcast, glaciers. Nord is pale and desaturated (frost
`88c0d0`, `81a1c1`, snow `eceff4`). Night auroras belong to cyan; frost keeps only `night-aurora-tundra`.
- Wallhaven: `ffffff`, `cccccc`, `66cccc`, `999999`. q: `snow`, `ice`, `glacier`, `winter`, `fog`.

## green (Everforest)
Forests, ferns, lush nature, terminal/matrix green. Everforest is soft sage (`a7c080`, aqua
`83c092`), so mossy, misty greens fit better than acid green.
- Wallhaven: `336600`, `669900`, `666600`, `77cc33`. q: `forest`, `moss`, `ferns`, `valley`.

## mono
Black and white, near-grey, a single small colour accent at most. Text-coloured accent, so nothing
in the UI is coloured.
- Wallhaven: `000000`, `424153`, `999999`, `cccccc`. q: `black and white`, `monochrome`, `minimalist`.

## pink (Dracula)
Loud: neon, synthwave, cyberpunk, magenta glow, saturated pink sunsets. Dracula pink `ff79c6`, purple
`bd93f9`, cyan `8be9fd` on `282a36`.
- Wallhaven: `ea4c88`, `993399`, `cc3333`. q: `synthwave`, `neon`, `pink sunset`, `cyberpunk`.

## purple (Catppuccin)
Quiet twilight: dusk, mist, night forests, fantasy, calm violet skies. Catppuccin is pastel (mauve
`cba6f7`, pink `f5c2e7`, blue `89b4fa`), so soft lavender over neon violet.
- Wallhaven: `663399`, `993399`, `333399`. q: `dusk`, `twilight`, `fantasy`, `mist`.

## red (Rosé Pine, true-red accent)
Crimson: blood moons, red shrines, fire. The accent `e5484d` is a true red; Rosé Pine's own "love"
`eb6f92` reads as pink next to the pink theme, so prefer crimson over rose.
- Wallhaven: `990000`, `cc0000`, `660000`. q: `red moon`, `shrine`, `samurai`, `crimson`.
