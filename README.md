# Corne ZMK Config
[![Build ZMK firmware](https://github.com/hendstephen/zmk-config/actions/workflows/build.yml/badge.svg)](https://github.com/hendstephen/zmk-config/actions/workflows/build.yml) [![Draw ZMK keymaps](https://github.com/hendstephen/zmk-config/actions/workflows/draw-keymaps.yml/badge.svg)](https://github.com/hendstephen/zmk-config/actions/workflows/draw-keymaps.yml)

This ZMK config is for split ergo 3x6 boards like the Corne. The repo also builds for the Lily58, ignoring the extra keys.  
* Keymap layout created with [@caksoylar's keymap-drawer](https://github.com/caksoylar/keymap-drawer).  
* This config uses [@urob's ZMK fork](https://github.com/urob/zmk) which contains a handful of tweaks and PRs that aren't yet merged into mainline ZMK.

## Features
- Colemak-DH base layer
- Homerow mods using [urob's timeless homerow mod config](https://github.com/urob/zmk-config?tab=readme-ov-file#timeless-homerow-mods)
- Symbol layer based on [gertreuer's symbol layer](https://github.com/getreuer/qmk-keymap?tab=readme-ov-file#my-keymap)
- Commonly used symbols in combos on the base layer
  - _These symbols are specific to my development workflow (C#/.NET, React, Typescript). While the symbol layer design is good, I found that switching back and forth to this layer while coding was awkward for me. Having my most used symbols on the base layer is much smoother, and I've tuned the combo timing so that misfires are not an issue. (For reference, I get few misfires at a typing speed of around ~100 wpm)._
  - _I've also struggled with some thumb pain/fatigue, so reducing thumb use as much as possible in favor of combos helps to minimize this._
- Sticky shift on pinkies
  - _Similar to above, this helps reduce the thumb fatigue that comes from having sticky shift on thumbs. I also could never quite get used to shift on my thumbs. My pinkies just want to reach out for shift._
- Numpad on the nav layer for vim line motions (e.g. `15↑` to jump up 15 lines)
- Num-word
- More intuitive [mod morphs](#mod-morphs)
- Convenience macros
  - `=>` or "fat arrow" 
  - Cut, Copy, Paste, Select all - All are left-hand only for easy editing while using the mouse.
  - Windows shortcuts
    - Lock: `Win + L`
    - Desktop left/right: `Win + Ctrl + Left/Right`
    - Close: `Alt + F4`
  - `ion` - outputs the common pattern "ion" in many english words, which for me is difficult to get right as it's an outward roll on the pinky
  - `../` - to `cd` up one level
  - `//` - long press on `/` key to output double slash for starting a comment
- Sticky `Alt` on base layer re: [Issue #759](https://github.com/zmkfirmware/zmk/issues/759)
  - _I do most of my work on a remote desktop, and it seems the client doesn't respect the `alt` modifier on a non-base layer (or mod-tap) until after the full tap-hold delay. I got tired of waiting, so I put sticky `alt` on the base layer as well as a tab combo for a quick window switch without waiting for the full timeout._
- `alt` layer for unicode/international characters
  - `u` key has hold/tap for spanish alts:
    - tap: `ú` (e.g. "tú")
    - hold: `ü` (e.g. "bilingüe")

![Keymap Representation](./keymap-drawer/corne.svg?raw=true "Keymap Representation")

## Mod Morphs
| Tap            | Shift + Tap | 
| -------------- | ----------- | 
| `.`            | `:`         | 
| `,`            | `;`         | 
| `/`            | `?`         |
| `⌫`            | `⌦`         | 
| `Sticky Shift` | `Caps Word` | 