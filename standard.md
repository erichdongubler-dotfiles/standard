# 0.2.0

This standard specifies @ErichDonGubler's preferred desktop environment as a set
of features and tiers. The remainder of this document will be written in
first-person.

## Why?

My particular flavor of neurodivergence (hello, fellow ADHDers!) makes lots of
little detail-oriented tasks take significantly longer than even a normal person
might need. I automate the setup of my desktop environments, but the
requirements of what I'd like to keep between platforms can be hard to keep
track of, esp. when automating a new platform. This document does that for me.

## Feature Sets

### Machine Productivity Tiers

Machine productivity depends greatly on what I can install onto a device. In
turn, this is dependent on how much influence I'm allowed over it. I've split
this into multipler tiers:

1. `minimal`: basically sufficient to use `git` to push changes to
   source control somewhere. Most useful for embedded devices or servers
   that I couldn't benefit from setting up a desktop environment
   for. Production debugging and fixing, for example.

1. `productive`: The majority of my environment, containing:
   1. Preferred input methods
   1. Screen capturing
   1. Web browsing ecosystem
   1. Software developer environment

   Suitable for environments where I'm allowed to install
   non-security-sensitive things, like corporate workstations that nominally
   belong to me.

1. `full`: The final difficult-to-obtain window management behaviors that
   I prefer, but aren't realistic in all graphical environments.

### `tailscale`

If I fully own the device, I also prefer to add add the `tailscale` feature
set. This is independent of machine productivity tier.

## Features

| Feature description                                                                   | `minimal` | `productive` | `full` | `tailscale` |
| ------------------------------------------------------------------------------------- | --------- | ------------ | ------ | ----------- |
| 1: Installs `git`, `patch`                                                            | ✔         | ✔            | ✔      | -           |
| 2: Installs an `ssh` client                                                           | ✔         | ✔            | ✔      | -           |
| 3: Installs [Erich's preferred binaries/applications][preferred-bins] and his config. | ❌        | ✔            | ✔      | -           |
| 4: Enables focus-follows-mouse                                                        | ❌        | ❌           | ✔      | -           |
| 5: Enables window dragging with a modifier key (preferably <kbd>Alt</kbd>)            | ❌        | ❌           | ✔      | -           |
| 6: Registers the device on Erich's personal `tailscale`                               | -         | -            | -      | ✔           |

[preferred-bins]: #preferred-binaries-applications

## Preferred binaries/applications

1. A terminal that supports subsequent terminal UIs, preferably
   [`wezterm`](https://github.com/wezfurlong/wezterm) with Erich's
   [`wezterm` dotfiles](https://github.com/erichdongubler-dotfiles/wezterm)
1. [Jujutsu](https://jj-vcs.dev)
1. [`bellboy`](https://github.com/erichdongubler/bellboy) -- for dotfiles
   management
1. [`nushell`](https://github.com/nushell/nushell), which implements
   [preferred shell features] with Erich's [`nushell` dotfiles
   repo](https://github.com/erichdongubler-dotfiles/nushell)
   1. The prompt for this shell is also preferred to be implemented via
      [`starship`](https://starship.rs), with Erich's [`starship`
      dotfiles
      repo](https://github.com/erichdongubler-dotfiles/starship)
1. [Neovim](https://github.com/neovim/neovim), with Erich's [`neovim`
   dotfiles repo](https://github.com/erichdongubler-dotfiles/neovim)
1. [`atuin`](https://github.com/atuinsh/atuin), with Erich's [`atuin` dotfiles
   repo](https://github.com/erichdongubler-dotfiles/atuin)
1. [`espanso`](https://espanso.org), with Erich's [`espanso` dotfiles
   repo](https://github.com/erichdongubler-dotfiles/espansoo)
1. `mdlink` with Erich's
   [`mdlink`](https://github.com/erichdongubler-dotfiles/mdlink)
   dotfiles
1. [`firefox`](https://firefox.com)
   repo](https://github.com/erichdongubler-dotfiles/espansoo)
1. [`fzf`](https://github.com/junegunn/fzf)
1. A good 3-way merge tool, preferably [`meld`](https://meldmerge.org/)
1. Cargo toolchain
   1. [`rustup`](https://rustup.rs)
   1. [`rust-analyzer`](https://rust-analyzer.github.io),
      likely through the correspondent `rustup` component
   1. [`cargo-binstall`](https://github.com/cargo-bins/cargo-binstall)
1. [`fd`](https://github.com/sharkdp/fd)
1. [`rg`](https://github.com/burntsushi/ripgrep)
1. [`delta`](https://github.com/dandavison/delta)
1. [`hexyl`](https://github.com/sharkdp/hexyl)
1. [`tokei`](https://github.com/XAMPPRocky/tokei)
1. [`watchexec`](https://github.com/watchexec/watchexec)
1. [`zoxide`](https://github.com/ajeetdsouza/zoxide)
1. [`mergiraf`](https://mergiraf.org/)
1. [`gh`](https://cli.github.com/)

[preferred shell features]: #preferred-shell-features

## Preferred shell features

1. Vi mode.
   1. Typical motions:
      1. <kbd>w</kbd>/<kbd>W</kbd>
      1. <kbd>b</kbd>/<kbd>B</kbd>
      1. <kbd>0</kbd>/<kbd>^</kbd>/<kbd>Home</kbd>
      1. <kbd>$</kbd>/<kbd>End</kbd>
      1. <kbd>f</kbd>/<kbd>F</kbd> + key
      1. <kbd>t</kbd>/<kbd>T</kbd> + key
   1. Fancier motions:
      1. <kbd>Ctrl</kbd> + arrow
   1. Typical operators:
      1. <kbd>c</kbd>/<kbd>C</kbd>
      1. <kbd>d</kbd>/<kbd>D</kbd>
      1. <kbd>i</kbd>/<kbd>I</kbd>
      1. <kbd>a</kbd>/<kbd>A</kbd>
   1. Basic text objects, `{a,i}` variants for:
      1. <kbd>]</kbd>
      1. <kbd>)</kbd>
      1. <kbd>}</kbd>
      1. <kbd>w</kbd>/<kbd>W</kbd>.
      1. <kbd>'</kbd>/<kbd>"</kbd>.
   1. Indication of editing mode via ANSI cursor shape manipulation.
1. Command history traversal: preferred flow is to press <kbd>Up</kbd> or
   <kbd>Down</kbd> to search based on what was already typed, maintaining
   cursor position throughout the process.
   1. <kbd>CTRL</kbd> + <kbd>R</kbd> is preferred to be bound to `atuin`.
1. Cross-platform scripting support.
