# Corne42 Handwired: Current Matrix + Keymap

This document reflects the current configuration in this repo for:
- `nice_nano` + `corne42_left`
- `nice_nano` + `corne42_right`

## Build Targets

From `build.yaml`:
- `board: nice_nano`, `shield: corne42_left`
- `board: nice_nano`, `shield: corne42_right`

## Matrix Summary

- Matrix size: **4 rows x 6 columns**
- Diode direction: **col2row**
- Main area uses rows 0..2, cols 0..5
- Thumb cluster uses 3 keys per half:
  - Left: `RC(3,3) RC(3,4) RC(3,5)`
  - Right: `RC(3,0) RC(3,1) RC(3,2)`

## Left Half (`corne42_left`)

### Row GPIOs (top -> bottom)

| Row index | GPIO pin |
|---|---|
| 0 | P1.00 |
| 1 | P0.11 |
| 2 | P1.04 |
| 3 | P1.06 |

### Column GPIOs (left -> right)

| Col index | GPIO pin |
|---|---|
| 0 | P0.09 |
| 1 | P1.11 |
| 2 | P0.10 |
| 3 | P0.02 |
| 4 | P1.15 |
| 5 | P1.13 |

### Keymap (`config/corne42_left.keymap`)

#### Base
- Row 0: `TAB Q W E R T`
- Row 1: `LCTRL A S D F G`
- Row 2: `LSHFT Z X C V B`
- Thumbs (`RC(3,3..5)`): `LGUI MO(1) SPACE`

#### Lower
- Row 0: `TAB 1 2 3 4 5`
- Row 1: `BT_CLR BT_SEL0 BT_SEL1 BT_SEL2 BT_SEL3 BT_SEL4`
- Row 2: `LSHFT TRANS TRANS TRANS TRANS TRANS`
- Thumbs (`RC(3,3..5)`): `LGUI TRANS SPACE`

#### Raise
- Row 0: `TAB ! @ # $ %`
- Row 1: `LCTRL TRANS TRANS TRANS TRANS TRANS`
- Row 2: `LSHFT TRANS TRANS TRANS TRANS TRANS`
- Thumbs (`RC(3,3..5)`): `LGUI TRANS SPACE`

## Right Half (`corne42_right`)

### Row GPIOs (top -> bottom)

| Row index | GPIO pin |
|---|---|
| 0 | P1.13 |
| 1 | P1.11 |
| 2 | P0.10 |
| 3 | P0.06 |

### Column GPIOs (right -> left)

| Col index | GPIO pin |
|---|---|
| 0 | P1.06 |
| 1 | P0.11 |
| 2 | P1.04 |
| 3 | P0.22 |
| 4 | P0.24 |
| 5 | P1.00 |

> Note: for the right half, index `col 0` is the **physical rightmost** column and `col 5` is the **physical leftmost** column.

### Keymap (`config/corne42_right.keymap`)

#### Base
- Row 0: `BSPC P O I U Y`
- Row 1: `SQT SEMI L K J H`
- Row 2: `ESC / . , M N`
- Thumbs (`RC(3,0..2)`): `RALT MO(2) RET`

#### Raise
- Row 0: `BSPC ) ( * & ^`
- Row 1: `` ` \ ] [ = - ``
- Row 2: `~ | } { + _`
- Thumbs (`RC(3,0..2)`): `RALT TRANS RET`

#### Lower
- Row 0: `BSPC 0 9 8 7 6`
- Row 1: `TRANS TRANS RIGHT UP DOWN LEFT`
- Row 2: `TRANS TRANS TRANS TRANS TRANS TRANS`
- Thumbs (`RC(3,0..2)`): `RALT TRANS RET`
