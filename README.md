# libass_sub_selector
Visually select individual subtitles a la PotPlayer.
[OldPreviewBeforeFork](https://too.lewd.se/bb9fafdc5a88_preview.mp4)
[FastMadePreview](https://github.com/AkuLinker/libass_sub_selector/raw/master/preview.mp4)

This is a Linux/Wayland fork of [po5/libass_sub_selector](https://github.com/po5/libass_sub_selector), reworked with the help of AI. Windows support has been dropped, clipboard integration changed to `wl-copy`.

**Note:** only ASS/SSA subtitles are supported.

## Requirements
- `libass`
- `ffmpeg`
- `mkvtoolnix-cli` (mkvmerge + mkvextract)
- `wl-clipboard` (wl-copy)

## Installation
Place `libass_sub_selector.lua` in your mpv `scripts` folder.

## Keybindings
No keys are bound by default. Add these to your `input.conf`:
```
<key> script-binding copy-subs
<key> script-binding toggle-bounds
```
`copy-subs` — hover over a subtitle and press the key to copy it to clipboard.  
`toggle-bounds` — show bounding boxes around all current subtitles at once.

## Configuration
Create `script-opts/libass_sub_selector.conf` in your mpv config folder:
```
# Path to libass shared library. Set this if the script can't find it automatically.
# libass_path=/usr/lib/libass.so.9

# Only highlight subtitles while paused (default: no)
paused_only=yes

# Highlight subtitle on mouse hover (default: yes)
on_hover=yes

# Hide highlight when cursor autohide kicks in (default: yes)
autohide=yes
```
