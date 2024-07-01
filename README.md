# Corne ZMK Config
This ZMK config is for split ergo 3x6 boards like the Corne. The repo also builds for the Lily58, ignoring the extra keys.

Keymap layout created with [@caksoylar's keymap-drawer](https://github.com/caksoylar/keymap-drawer)

## Features
- Colemak-DH base layer
- Homerow mods using [urob's timeless homerow mod config](https://github.com/urob/zmk-config?tab=readme-ov-file#timeless-homerow-mods)
- Symbol layer based on [gertreuer's symbol layer](https://github.com/getreuer/qmk-keymap?tab=readme-ov-file#my-keymap)
- Commonly used symbols in combos on the base layer
  - _These symbols are specific to my development workflow (C#/.NET, React, Typescript). While the symbol layer design is good, I found that switching back and forth to this layer while coding was awkward for me. Having my most used symbols on the base layer is much smoother, and I've tuned the combo timing so that misfires are not an issue._
  - _I've also struggled with some thumb pain/fatigue, so reducing thumb use as much as possible in favor of combos helps to minimize this._
- Numpad on the nav layer for vim line motions (e.g. `15↑` to jump up 15 lines)
- More intuitive [mod morphs](#mod-morphs)
- Convenience macros
  - `ion` - Chording the `i`, `o`, and `n` keys at the same time outputs the common, but (for me) tricky outward roll of "ion".
  - `=>` or "fat arrow" - Used all the time in React/TypeScript (and some what regularly in C#), this macro outputs `=>` in a single keystroke, which I use as a combo on the base layer.
  - `../` - One keystroke to `cd` up one directory
  - Cut, Copy, Paste, Select all - All are left-hand only for easy editing while using the mouse.

![Keymap Representation](./keymap-drawer/corne.svg?raw=true "Keymap Representation")

## Mod Morphs
| Tap            | Shift + Tap | Ctrl + Shift + Tap |
| -------------- | ----------- | ------------------ |
| `.`            | `:`         | `_`                |
| `,`            | `;`         | `-`                |
| `/`            | `?`         | `!`                |
| `␣`            | `⌫`         |                    |
| `⌫`            | `⌦`         |                    |
| `Sticky Shift` | `Caps Word` |                    |