## Erich's personal development platform

This repo is used by @ErichDonGubler to keep track of the features of the
personal development platform he likes across all his machines.

# 0.1.0

This standard specifies the following tiers of support for Erich's personal
development, which are, at a high level:

1. `minimal`: basically sufficient to use `git` to push changes to source
	control somewhere. Most useful for specifying what Erich needs to work on
	non-development machines for short periods of time, like production
	debugging and fixing.
2. `full`: Erich's good to go!
	1. Fully supports the latest stable Rust toolchain.
	2. Able to install [applications and binaries that Erich
	    prefers][preferred-bins] to always have available.

Features of each platform support tier are listed in the following table:

| Feature\tier of support                                                                        | `minimal` | `full` |
| ---------------------------------------------------------------------------------------------- | --------- | ------ |
| 1: Installs `git`                                                                              | [x]       | [x]    |
| 2: Installs `openssh`                                                                          | [x]       | [x]    |
| 3: Auto-installs [Erich's preferred binaries and applications][preferred-bins]                 | [ ]       | [x]    |
| 4: Installs and configures a [shell with Erichs' preferred features][preferred-shell-features] | [ ]       | [x]    |
| 5: Enables focus-follows-mouse                                                                 | [ ]       | [x]    |
| 6: Enables alt-dragging                                                                        | [ ]       | [x]    |

[preferred-bins]: #preferred-binaries-applications
[preferred-shell-features]: #preferred-shell-features

## Preferred binaries/applications

1. [`capisco`](https://github.com/erichdongubler/capisco) -- for dotfiles
    management, used quite a bit below.
2. `neovim`, in tandem with the [`neovim` dotfiles
    repo](https://github.com/erichdongubler-dotfiles/neovim).
3. [`fd`](https://github.com/sharkdp/fd)
4. [`rg`](https://github.com/burntsushi/ripgrep)
5. [`firefox`](https://firefox.com)
6. [`fzf`](https://github.com/junegunn/fzf)
7. Cargo toolchain
	1. [`rust-analyzer`](https://rust-analyzer.github.io)
	2. [`rustup`](https://rustup.rs)
8. [`p4merge`](https://www.perforce.com/products/helix-core-apps/merge-diff-tool-p4merge)
9. [Visual Studio Code](https://code.visualstudio.com/)
10. [`hexyl`](https://github.com/sharkdp/hexyl)
11. [`tokei`](https://github.com/XAMPPRocky/tokei)
12. [`watchexec`](https://github.com/watchexec/watchexec)
13. [`rescuetime`](https://rescuetime.com)
14. [Telegram](https://telegram.org)
15. [Discord](https://discord.com)

## Preferred shell features

1. Vi mode.
	1. Typical motions:
		1. <kbd>w</kbd>/<kbd>W</kbd>
		2. <kbd>b</kbd>/<kbd>B</kbd>
		3. <kbd>0</kbd>/<kbd>^</kbd>/<kbd>Home</kbd> 
		4. <kbd>$</kbd>/<kbd>End</kbd>
		5. <kbd>f</kbd>/<kbd>F</kbd> + key
		6. <kbd>t</kbd>/<kbd>T</kbd> + key
	2. Fancier motions:
		1. <kbd>Ctrl</kbd> + arrow
	3. Typical operators:
		1. <kbd>c</kbd>/<kbd>C</kbd>
		2. <kbd>d</kbd>/<kbd>D</kbd>
		3. <kbd>i</kbd>/<kbd>I</kbd>
		4. <kbd>a</kbd>/<kbd>A</kbd>
	4. Basic text objects, `{a,i}` variants for:
		1. <kbd>]</kbd>
		2. <kbd>)</kbd>
		3. <kbd>}</kbd>
		4. <kbd>w</kbd>/<kbd>W</kbd>.
	5. Indication of editing mode via ANSI cursor shape manipulation.
2. Completion with reasonable coverage of:
	1. `git`
	2. Bonus: other commands providing a standard completion format?
3. Command history traversal: preferred flow is to press <kbd>Up</kbd> or
    <kbd>Down</kbd> to search based on what was already typed, maintaining
    cursor position throughout the process.
4. Cross-platform scripting support, for use with `git`.
