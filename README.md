# Jacob's Build of the simple terminal by [suckless](https://st.suckless.org)

## Patches

- [gruvbox dark](https://st.suckless.org/patches/gruvbox/)

- [boxdraw](https://st.suckless.org/patches/boxdraw/)

- [externalpipe](https://st.suckless.org/patches/externalpipe/)

- [xclearwin](https://st.suckless.org/patches/xclearwin/)

- [one clipboard](https://st.suckless.org/patches/clipboard/)

- [Alpha Focus Highlight](https://st.suckless.org/patches/alpha_focus_highlight/)

- [font2](https://st.suckless.org/patches/font2/
)
- [New terminal in current directory](https://st.suckless.org/patches/newterm/)

- [Scrollback](https://st.suckless.org/patches/scrollback/)

- [vertcenter](https://st.suckless.org/patches/vertcenter/)

- [xresources](https://st.suckless.org/patches/xresources/)

- uses Luke Smith's [st-copyout](https://github.com/LukeSmithxyz/st/blob/master/st-copyout) and [st-urlhandler](https://github.com/LukeSmithxyz/st/blob/master/st-urlhandler) scripts

## Keybinds

- **RTFM**

## Installation

```shell
git clone https://gitlab.com/Jacob_McDonnell/st.git
cd st
sudo make install
```

Users of Arch-based distros can install from the AUR, [st-jacob-git](https://aur.archlinux.org/packages/st-jacob-git/).

## Dependencies

- `xurls` for using the url features

- `xclip` for copying and pasting

- Any compositor for the alpha (`xcompmgr`, `compton`, etc.)

- `dmenu` for the url and copying prompts

- `fontconfig` for the default font

- `pywal` for a dynamic color scheme

- [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/), but libxft-bgra does not install for me

- `ttf-joypixels`

## How to configure with Xresources

Many variables can be configured through `~/.Xdefaults` or `~/Xresources` but you must run `xrdb` on the file before the settings load.

For example fonts, transparency, or colors:

```
*.font:	IBM Plex Mono:pixelsize=14:antialias=true:autohint=true;
*.alpha: 0.9
*.color0: #111
```

The `alpha` value is for transparency and goes from 0(transparent) to 1(opaque).

### Colors and Fonts

- By default this will use [gruvbox dark](https://github.com/morhetz/gruvbox)

- Compatible with `Xresources` and `pywal` for a dynamic color scheme

- Default font is the default mono font of your system at size 14pt and uses `ttf-joypixels`  for emojis

## Emojis

st like many suckless programs will crash at the first sign of an emoji. The solutions to this is to install [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/)
