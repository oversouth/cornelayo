# ZMK 42-key to W-Corne 46-key Mapping - Final Corrected Version

## W-Corne 46-key Layout Structure
Each row in the .vil file is a 12-element array where:
- Positions 0-5: Left half keys
- Positions 6-11: Right half keys

```
Row 0 (Top):    [0:Tab] [1:Q] [2:W] [3:E] [4:R] [5:T] | [6:RCtrl*] [7:Y] [8:U] [9:I] [10:O] [11:P]
Row 1 (Middle): [0:LCtrl] [1:A] [2:S] [3:D] [4:F] [5:G] | [6:RAlt*] [7:H] [8:J] [9:K] [10:L] [11:;]
Row 2 (Bottom): [0:LShift] [1:Z] [2:X] [3:C] [4:V] [5:B] | [6:-1] [7:N] [8:M] [9:,] [10:.] [11:/]
Row 3 (Thumbs): [0:LCtrl*] [1:LAlt*] [2:-1] [3:LGui] [4:Enter] [5:Space] | [6:Space] [7:Del] [8:RGui] [9:Bksp*] [10:Quote*] [11:Esc*]

* = Extra keys not present in standard 42-key Corne
```

## Physical Layout with Extra Keys Highlighted
```
Left Half:                                    Right Half:
┌─────┬─────┬─────┬─────┬─────┬─────┐  ┌─────┬─────┬─────┬─────┬─────┬─────┐
│ Tab │  Q  │  W  │  E  │  R  │  T  │  │RCtrl│  Y  │  U  │  I  │  O  │  P  │
│ [0] │ [1] │ [2] │ [3] │ [4] │ [5] │  │ [6]*│ [7] │ [8] │ [9] │[10] │[11] │
├─────┼─────┼─────┼─────┼─────┼─────┤  ├─────┼─────┼─────┼─────┼─────┼─────┤
│LCtrl│  A  │  S  │  D  │  F  │  G  │  │RAlt │  H  │  J  │  K  │  L  │  ;  │
│ [0] │ [1] │ [2] │ [3] │ [4] │ [5] │  │ [6]*│ [7] │ [8] │ [9] │[10] │[11] │
├─────┼─────┼─────┼─────┼─────┼─────┤  ├─────┼─────┼─────┼─────┼─────┼─────┤
│LShft│  Z  │  X  │  C  │  V  │  B  │  │  -  │  N  │  M  │  ,  │  .  │  /  │
│ [0] │ [1] │ [2] │ [3] │ [4] │ [5] │  │ [6] │ [7] │ [8] │ [9] │[10] │[11] │
└─────┴─────┴─────┼─────┼─────┼─────┤  ├─────┼─────┼─────┼─────┴─────┴─────┘
  [0]*  [1]*      │LGui │Enter│Space│  │Space│ Del │RGui │    [9]*  [10]* [11]*
  LCtrl LAlt      │ [3] │ [4] │ [5] │  │ [6] │ [7] │ [8] │    Bksp  Quote  Esc
                  └─────┴─────┴─────┘  └─────┴─────┴─────┘

* = Extra keys in W-Corne (4 total: RCtrl, RAlt, and 2 extra left thumb keys)
```

## ZMK 42-key to W-Corne 46-key Mapping

### Main Key Mapping (ZMK position → W-Corne array position):
```
Left Half:
ZMK  0 (Tab)     → Row0[0]
ZMK  1 (Q)       → Row0[1]
ZMK  2 (W)       → Row0[2]
ZMK  3 (E)       → Row0[3]
ZMK  4 (R)       → Row0[4]
ZMK  5 (T)       → Row0[5]

ZMK 10 (Ctrl/A)  → Row1[0]
ZMK 11 (S)       → Row1[1]
ZMK 12 (D)       → Row1[2]
ZMK 13 (F)       → Row1[3]
ZMK 14 (G)       → Row1[5]

ZMK 20 (LShift)  → Row2[0]
ZMK 21 (Z)       → Row2[1]
ZMK 22 (X)       → Row2[2]
ZMK 23 (C)       → Row2[3]
ZMK 24 (V)       → Row2[4]
ZMK 25 (B)       → Row2[5]

ZMK 30 (GUI)     → Row3[3]
ZMK 31 (Lower)   → Row3[4]
ZMK 32 (Space)   → Row3[5]

Right Half:
ZMK  5 (Y)       → Row0[7]
ZMK  6 (U)       → Row0[8]
ZMK  7 (I)       → Row0[9]
ZMK  8 (O)       → Row0[10]
ZMK  9 (P)       → Row0[11]

ZMK 15 (H)       → Row1[7]
ZMK 16 (J)       → Row1[8]
ZMK 17 (K)       → Row1[9]
ZMK 18 (L)       → Row1[10]
ZMK 19 (;)       → Row1[11]

ZMK 25 (N)       → Row2[7]
ZMK 26 (M)       → Row2[8]
ZMK 27 (,)       → Row2[9]
ZMK 28 (.)       → Row2[10]
ZMK 29 (/)       → Row2[11]

ZMK 33 (Space)   → Row3[6]
ZMK 34 (Bksp)    → Row3[7]
ZMK 35 (GUI)     → Row3[8]

Extra W-Corne Keys (to be configured):
Row0[6] - RCtrl (right inner column top)
Row1[6] - RAlt (right inner column middle)
Row3[0] - LCtrl (extra left thumb)
Row3[1] - LAlt (extra left thumb)
```

### Key Features to Convert:
1. **Home Row Mods**: A,S,D,F (left) and J,K,L,; (right) with hold-tap behaviors
2. **Tap Dance**: Left Shift doubles as Enter on double-tap
3. **Layer Keys**: Thumb keys activate layers on hold
4. **Combos**: 15 different key combinations
5. **Macros**: Lambda, brackets, paste_enter functions