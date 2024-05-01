# Lily58 ZMK Config
## Features
- Homerow mods using [urob's timeless homerow mod feature](https://github.com/urob/zmk-config?tab=readme-ov-file#timeless-homerow-mods)
- Symbol layer based on [gertreuer's symbol layer](https://github.com/getreuer/qmk-keymap?tab=readme-ov-file#my-keymap)
- Tri-state window swapper (requires [PR #1366](https://github.com/zmkfirmware/zmk/pull/1366))
- Commonly used symbols in combos on the base layer
  - _These symbols are specific to my development workflow (C#/.NET, React, Typescript). While the symbol layer design is good, I found that switching back and forth to this layer while coding was awkward for me. Having my most used symbols on the base layer is much smoother, and I've tuned the combo timing so that misfires are not an issue._
- Numpad on the nav layer for vim line motions (e.g. `15↑` to jump up 15 lines)
- Sticky shift > caps word > caps lock mod morph

![Keymap Representation](./keymap-drawer/lily58.svg?raw=true "Keymap Representation")

