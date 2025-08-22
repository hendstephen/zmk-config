# Corne ZMK Config
[![Build ZMK firmware](https://github.com/hendstephen/zmk-config/actions/workflows/build.yml/badge.svg)](https://github.com/hendstephen/zmk-config/actions/workflows/build.yml) [![Draw ZMK keymaps](https://github.com/hendstephen/zmk-config/actions/workflows/draw-keymaps.yml/badge.svg)](https://github.com/hendstephen/zmk-config/actions/workflows/draw-keymaps.yml)

This ZMK config is for split ergo 3x6 boards like the Corne. The repo also builds for the Lily58, ignoring the extra keys.  
* Keymap layout created with [@caksoylar's keymap-drawer](https://github.com/caksoylar/keymap-drawer).  
* [ZMK Zephyr modules](https://zmk.dev/docs/features/modules) used to add certain features (helpers, num word, etc)
* nice!view customization via [@M165437's nice-view-gem](https://github.com/M165437/nice-view-gem)

## Features
- Colemak-DH base layer (_see section on [night](#night-layout)_)
- Homerow mods using [urob's timeless homerow mod config](https://github.com/urob/zmk-config?tab=readme-ov-file#timeless-homerow-mods)
- Symbol layer based on [getreuer's symbol layer](https://github.com/getreuer/qmk-keymap?tab=readme-ov-file#my-keymap)
- Commonly used symbols in combos on the base layer (_see section on [combos](#symbol-combos)_)
- Sticky shift on pinkies
- Numpad on the nav layer for vim line motions (e.g. `15↑` to jump up 15 lines)
  - _This is needed mainly because I use an alt layout and thus lose the typical `hjkl` home row navigation._
  - _Additionally, having a nav block on the home row is very convenient even in non-vim scenarios._
- Num-word
- More intuitive [mod morphs](#mod-morphs)
- Convenience macros
  - `=>` or "fat arrow" 
  - Cut, Copy, Paste, Select all - All are left-hand only for easy editing while using the mouse.
  - `//` - long press on `/` key to output double slash for starting a comment
- Sticky `Alt` on base layer re: [Issue #759](https://github.com/zmkfirmware/zmk/issues/759)
  - _I do most of my work on a remote desktop, and it seems the client doesn't respect the `alt` modifier on a non-base layer (or mod-tap) until after the full tap-hold delay. I got tired of waiting, so I put sticky `alt` on the base layer as well as a tab combo for a quick window switch without waiting for the full timeout._

## Keymap
![Keymap Representation](./keymap-drawer/corne.svg?raw=true "Keymap Representation")

## Night Layout
I'm in the process of switching to Valorance's [night layout](https://luminespire.github.io/night/home.html), with some changes.  
ASCII version of my variant:
```
x f l d v  p w o u ,
n s h t m  y c a e i
b z j k q  ' g ; / .
        r
```

### BX swap
I'm not a fan of top row pinkies (QWERTY `q` position) on my corne, because it forces me to move my whole hand up. I swap `b` with `x` to put it in the bottom row. With some other similar layouts that use a `bnx` column and have `l` on the left hand (gallium, graphite), this would cause a bad scissor because of the `l` position on the top ring, but with night's `l` being on the top middle instead of ring it feels fine.

### Left Hand
I use the nightingale left hand, which notably:
- Puts `d` on top instead of `k`
- Swaps `vqz` in order to put `v` on the top corner to minimize movement from `d_v` and `l_v` skipgrams

## Symbol Combos
I much prefer combos over layers. There is less interruption to my typing flow that comes from swapping to a layer. This is particularly true when inputting a single symbol (e.g. `=` vs `=>`), in which case holding a layer is very awkward. This can be worked around by using a one-shot layer key for the symbol layer, but then you have to account for both a one-shot symbol (`=`) and a two-shot (or even n-shot) symbol (`=>`). This is less than ideal, so for this reason I have all symbols on combos on the base layer.

Additionally, my most common symbols are duplicated on both hands to further improve typing flow when inputting symbols. For example, take this text:
```csharp
x >= 0;
```
Without `=` on both hands, this could result in the `>` and `=` combos being on the same hand. Putting `=` on both sides allows us to preserve alternation. Similarly, `;` is used all the time (at least in C-type languages), but often comes after either `)` or a letter. So, for the following lines, without `;` on both sides, at least one of these would result in an awkward same-hand combo sequence.
```csharp
CallFunc();         // Could be avoided by just having ) and ; combos on opposite hands
var x = myOtherVar; // No guarantee that the last letter will be on opposite hand from ;
```

## Mod Morphs
| Tap            | Shift + Tap | 
| -------------- | ----------- | 
| `.`            | `:`         | 
| `,`            | `;`         | 
| `/`            | `?`         |
| `⌫`            | `⌦`         | 
| `Sticky Shift` | `Caps Word` | 
