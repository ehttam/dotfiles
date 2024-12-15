# XREMAP

## Input

https://www.reddit.com/r/hyprland/comments/19b4vyq/how_do_you_remap_arrow_keys_to_ijkl_and_make_use/
https://github.com/xremap/xremap?tab=readme-ov-file#virtual_modifiers

## SETUP

1. Download https://github.com/xremap/xremap/releases/download/v0.10.2/xremap-linux-x86_64-hypr.zip

2. Move to bin to e.g. `/usr/local/bin`

3. Start xremap on hypr startup and use config.yml

config.yml
```
virtual_modifiers:
  - CapsLock
keymap:
  - remap:
      CapsLock-i: Up
      CapsLock-j: Left
      CapsLock-k: Down
      CapsLock-l: Right
```
