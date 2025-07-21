# ZMK to Vial Conversion Guide for W-Corne

## Overview
This guide documents the conversion of your 42-key ZMK Corne configuration to a 46-key W-Corne Vial configuration.

## Key Features Converted

### 1. Home Row Mods
- **ZMK**: Used hold-tap behaviors (HML/HMR)
- **Vial**: Converted to QMK Mod-Tap functions
  - A: `LCTL_T(KC_A)` - Hold for Left Control, tap for A
  - S: `LALT_T(KC_S)` - Hold for Left Alt, tap for S
  - D: `LGUI_T(KC_D)` - Hold for Left GUI, tap for D
  - F: `LSFT_T(KC_F)` - Hold for Left Shift, tap for F
  - J: `RSFT_T(KC_J)` - Hold for Right Shift, tap for J
  - K: `RGUI_T(KC_K)` - Hold for Right GUI, tap for K
  - L: `RALT_T(KC_L)` - Hold for Right Alt, tap for L
  - ;: `RCTL_T(KC_SCLN)` - Hold for Right Control, tap for ;

### 2. Tap Dance
- **TD(0)**: Left Shift that becomes Enter on double-tap
  - Single tap: Left Shift
  - Double tap: Enter

### 3. Layer Keys
- **LT(1,KC_ENT)**: Hold for Layer 1 (Lower), tap for Enter
- **LT(2,KC_SPC)**: Hold for Layer 2 (SpaceFN), tap for Space

### 4. Layers
- **Layer 0**: Base QWERTY with home row mods
- **Layer 1**: Lower - Numbers, F-keys, symbols
- **Layer 2**: SpaceFN (Raise) - Navigation, arrows, brackets
- **Layer 3**: Volume controls and delete
- **Layer 4**: Bluetooth (converted to empty layer - QMK uses different BT system)

### 5. Combos (First 5 implemented)
1. **V+B**: Paste Enter macro (M(0))
2. **C+D**: Copy (KC_LCMD)
3. **Z+X**: Print Screen (KC_PSCR)
4. **W+R**: Tab (KC_TAB)
5. **W+E**: Toggle Layer 4 (TG(4))

### 6. Macros
1. **Macro 0**: Paste Enter - Ctrl+V, Enter
2. **Macro 1**: Lambda Sign - "=>"
3. **Macro 2**: Lambda X - "\x"
4. **Macro 3**: Brackets - "[]" with cursor between

## Extra Keys Configuration
The W-Corne's 4 additional keys are currently set to:
- **Row 0, Position 6**: KC_NO (available for custom use)
- **Row 1, Position 6**: KC_NO (available for custom use)
- **Row 3, Position 0**: KC_NO (available for custom use)
- **Row 3, Position 1**: KC_NO (available for custom use)

You can customize these in Vial to add:
- Additional layer toggles
- Media controls
- Hyper/Meh keys
- Frequently used symbols

## How to Use

1. **Load the Configuration**:
   - Open Vial
   - Connect your W-Corne keyboard
   - Go to File → Load Current Layout
   - Select `zmk-to-vial-config.vil`

2. **Customize Extra Keys**:
   - The 4 extra keys are set to KC_NO
   - Click on them in Vial to assign functions

3. **Adjust Settings**:
   - Tap dance timing can be adjusted in the Tap Dance tab
   - Combo timing is preserved from your ZMK config

## Differences from ZMK

1. **Bluetooth**: QMK/Vial uses a different Bluetooth system. Layer 4 is empty and can be repurposed.
2. **Timing**: Hold-tap timings may feel slightly different. Adjust in QMK Settings tab if needed.
3. **Extra Keys**: You now have 4 additional keys to customize!

## Troubleshooting

- If home row mods are triggering too easily, increase the tapping term in QMK Settings
- If tap dance isn't working, check the tap dance timeout setting
- For combo issues, verify the combo term matches your preference

*Collaboration by Claude*