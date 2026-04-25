# Totem Keyboard - ZMK Firmware Configuration

![Icon](icon.png)

Custom ZMK firmware configuration for the [GEIST Totem](https://github.com/GEIGEIGEIST/TOTEM) split keyboard with Seeeduino XIAO BLE controllers.

## Features

- **Mouse Support** - Full pointer device support with mouse movement, clicking, and scrolling
- **ZMK Studio** - Live keymap editing without reflashing (with locking enabled for security)
- **NKRO** - N-key rollover enabled for better gaming and typing performance
- **4 Layers** - Base (QWERTY), Symbol, Navigation, and Adjust layers
- **Sticky Keys** - One-shot modifiers for ergonomic modifier usage
- **Caps Word** - Smart capitalization mode
- **Bluetooth** - Multi-device pairing support

## Layout Overview

- **Base Layer**: Standard QWERTY layout
- **Symbol Layer**: Brackets, operators, and special characters (activated via left thumb)
- **Navigation Layer**: Arrow keys, mouse controls, and number pad (activated via right thumb)  
- **Adjust Layer**: Media controls, Bluetooth settings, and function keys (both thumbs)

## Customizing the Keymap

1. Edit the `config/totem.keymap` file
   - Find available keycodes in the [ZMK documentation](https://zmk.dev/docs/keymaps/list-of-keycodes)
2. Commit and push your changes to GitHub
3. GitHub Actions will automatically build the firmware
4. Download the `firmware.zip` artifact from the Actions tab

## Flashing Instructions

### Left Half
1. Connect the left half of the keyboard to your computer via USB
2. Press the reset button twice quickly to enter bootloader mode
3. The keyboard will appear as a USB mass storage device
4. Drag and drop `totem_left-seeeduino_xiao_ble-zmk.uf2` onto the drive
5. The keyboard will automatically reboot with the new firmware

### Right Half
1. Repeat the same process with the right half
2. Use the `totem_right-seeeduino_xiao_ble-zmk.uf2` file

### Troubleshooting
If you encounter any issues, flash the settings reset firmware first, then flash the normal firmware again.

## ZMK Studio

With ZMK Studio enabled, you can edit your keymap in real-time using the [ZMK Studio web interface](https://zmk.studio) without needing to reflash the firmware.
