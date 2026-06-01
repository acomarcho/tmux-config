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
