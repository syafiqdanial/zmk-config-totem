# TOTEM keymap

This document maps the active keymap in [`config/totem.keymap`](../config/totem.keymap).

## Legend

- Combined labels use **tap / hold** order. For example, `A/GUI` taps `A` and holds Left GUI.
- `·` is disabled on that layer.
- `▽` is transparent and falls through to the active lower layer.
- The far-left and far-right keys on the third row are the physical side keys.

## Layer access

| Layer | Activation |
|---|---|
| BASE | Default |
| NAV | Hold `Space` |
| SYM | Hold `N` or hold `Tab` |
| BLU | Hold `Space + Backspace` together within 50 ms |

## Base layer

```text
                 LEFT HALF                              RIGHT HALF

          Q       W       E       R       T       Y       U       I       O       P
          A/GUI   S/Alt   D/Ctrl  F/Shift G       H       J/Shift K/Ctrl  L/Alt   '/;
   F2     Z       X       C       V       B       N/SYM   M       ,       .       //\     F4
                          Esc     Tab/SYM Space/NAV Backsp  Delete  Enter
```

Special hold-taps are intentionally preserved:

| Key label | Tap | Hold |
|---|---|---|
| `'/;` | Apostrophe | Semicolon |
| `//\` | Forward slash | Backslash |
| `N/SYM` | `N` | SYM layer |
| `Tab/SYM` | Tab | SYM layer |
| `Space/NAV` | Space | NAV layer |

The physical side keys remain `F2` and `F4`.

## Navigation layer

Hold `Space` to activate this layer. The left half remains a one-handed number pad; the right half remains the navigation cluster.

```text
                 LEFT HALF                              RIGHT HALF

          KP+     1       2       3       (       )       Home    Up      End     PgUp
          KP-     4       5       6       0       =       Left    Down    Right   PgDn
   Home   KP*     7       8       9       .       ·       Caps    NumLock ·       ·       End
                          KP/     F4/F2   ▽       Backsp  Delete  Enter
```

`F4/F2` taps `F4` and holds `F2`. Caps Lock and Num Lock sit directly below the arrow-key area.

## Symbol layer

Hold either `N` or `Tab` to activate this layer.

```text
                 LEFT HALF                              RIGHT HALF

          ()      []      {}      `       ~       ^       F1      F2      F3      F4
          !       @       #       $       |       ▽       F5      F6      F7      F8
   ·      %       ^       &       \       _       ▽       F9      F10     F11     F12     ·
                          ·       ·       ·       ·       ·       ·
```

- `[]` and `{}` place the cursor inside the pair.
- `()` leaves the cursor after the pair.
- The symbol and function-key bindings are unchanged.

## Bluetooth layer

Hold `Space + Backspace`, then press the required action key while continuing to hold the combo.

```text
                 LEFT HALF                              RIGHT HALF

          BT 0    BT 1    BT 2    BT 3    BT 4    ·       ·       ·       Clear   ·
          ·       ·       ·       ·       ·       ·       Vol-    Vol+    Bri-    Bri+
   ·      ·       ·       ·       ·       Boot L  Boot R  ·       ·       ·       ·       ·
                          Reset   ▽       ▽       ▽       ▽       Reset
```

Physical-key reference:

| Action | Physical key |
|---|---|
| Select Bluetooth profile 0–4 | `Q`, `W`, `E`, `R`, `T` |
| Clear the selected profile | `O` |
| Volume down/up | `J`, `K` |
| Brightness down/up | `L`, `;` |
| Bootloader left/right half | `B`, `N` |
| System reset | `Esc` or `Enter` |

> `BT Clear` clears only the currently selected profile. Reset and bootloader actions are intentionally kept on the maintenance layer.

## Removed scroll layer

The former pointer-scroll layer was removed because this TOTEM does not have a trackball. Backspace is now a normal key while still participating in the `Space + Backspace` Bluetooth combo.
