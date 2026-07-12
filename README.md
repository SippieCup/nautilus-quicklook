# nautilus-quicklook

A lightweight previewer for GNOME Files (Nautilus). Renders Markdown as
formatted text and previews images, text and source code, PDF, video, audio,
and fonts. Nautilus activates it on Space.

## Install

```
paru -S nautilus-quicklook-git
```

The base install covers Markdown, text, images, and fonts. Optional backends:

```
sudo pacman -S qt6-webengine              # PDF
sudo pacman -S qt6-multimedia             # video and audio
sudo pacman -S qt6-imageformats qt6-svg   # WebP/TIFF/AVIF, SVG
```

A missing optional backend shows a note naming the package to install.

## sway / i3

The window runs under XWayland with `WM_CLASS` `nautilus-quicklook`. Float it:

```
for_window [class="nautilus-quicklook"] floating enable
```

On sway, append `, move position center`.

## Options

- `QUICKLOOK_NO_AUTOHIDE`: keep the preview open when it loses focus. By default
  it closes on focus loss; Escape and Space also close it.

## License

MIT.
