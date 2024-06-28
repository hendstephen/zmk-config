# Corne ZMK Config
This ZMK config is for split ergo 3x6 boards like the Corne. The repo also builds for the Lily58, ignoring the extra keys.

## Features
- Colemak-DH base layer
- Homerow mods using [urob's timeless homerow mod feature](https://github.com/urob/zmk-config?tab=readme-ov-file#timeless-homerow-mods)
- Symbol layer based on [gertreuer's symbol layer](https://github.com/getreuer/qmk-keymap?tab=readme-ov-file#my-keymap)
- Commonly used symbols in combos on the base layer
  - _These symbols are specific to my development workflow (C#/.NET, React, Typescript). While the symbol layer design is good, I found that switching back and forth to this layer while coding was awkward for me. Having my most used symbols on the base layer is much smoother, and I've tuned the combo timing so that misfires are not an issue._
  - _I'm also currently trying to work through some fatigue/soreness in my thumbs. Using lighter switches on these keys seems to be helping, but I want to reduce the use of thumbs as layer holds as much as possible, thus the base layer combos._
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