# tmux-config

My personal [tmux](https://github.com/tmux/tmux) configuration.

## Highlights

- **Prefix remapped to `Ctrl-a`** (instead of the default `Ctrl-b`)
- Mouse support, 50k-line scrollback, and snappier key response
- Intuitive splits: `|` for horizontal, `-` for vertical (both keep the current directory)
- Vim-style pane navigation (`h/j/k/l`) and resizing (`Shift-H/J/K/L`)
- Windows and panes numbered from `1`, with automatic renumbering
- True color (24-bit) support
- vi-style keys in copy mode
- **[Catppuccin](https://github.com/catppuccin/tmux) Mocha** status bar theme
- Session save/restore with **[tmux-resurrect](https://github.com/tmux-plugins/tmux-resurrect)** and automatic saving via **[tmux-continuum](https://github.com/tmux-plugins/tmux-continuum)** (restores on server start)

## Install

You need [tmux](https://github.com/tmux/tmux/wiki/Installing) installed first (e.g. `brew install tmux` on macOS).

Then copy the config into your home directory:

```sh
git clone https://github.com/acomarcho/tmux-config.git
cp tmux-config/.tmux.conf ~/.tmux.conf
```

Or symlink it so you can keep it under version control:

```sh
ln -s "$(pwd)/tmux-config/.tmux.conf" ~/.tmux.conf
```

## Plugins

This config uses [TPM](https://github.com/tmux-plugins/tpm) (the tmux plugin manager) to manage:

- `tmux-plugins/tmux-resurrect` — manually save/restore sessions
- `tmux-plugins/tmux-continuum` — auto-save every 15 min and restore on server start
- `catppuccin/tmux` — Catppuccin Mocha status bar theme

Install TPM, then install the plugins:

```sh
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

Then start (or reload) tmux and press `Ctrl-a` + `I` (capital i) to fetch the plugins.

## Apply

If tmux is already running, reload the config with the prefix bind:

```
Ctrl-a r
```

Otherwise it loads automatically the next time you start tmux.

## Key bindings

The prefix is `Ctrl-a`. Press it, then:

| Binding            | Action                                   |
| ------------------ | ---------------------------------------- |
| `r`                | Reload the config                        |
| `\|`               | Split pane horizontally                  |
| `-`                | Split pane vertically                    |
| `c`                | New window (in current directory)        |
| `h` / `j` / `k` / `l` | Move to pane left/down/up/right       |
| `H` / `J` / `K` / `L` | Resize pane (repeatable)              |
| `Enter`            | Enter copy mode                          |
| `I`                | Install plugins (TPM)                    |
| `Ctrl-s`           | Save session (tmux-resurrect)            |
| `Ctrl-r`           | Restore session (tmux-resurrect)         |
