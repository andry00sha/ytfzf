<p align="center">
    <a> <img src=.assets/logo.png></a>
    <br />
    <br />
	<a href="https://github.com/pystardust/ytfzf/stargazers"><img src="https://img.shields.io/github/stars/pystardust/ytfzf?color=orange&logo=github&style=flat-square"></a>
	<a href="https://github.com/pystardust/ytfzf/graphs/contributors"><img src="https://img.shields.io/github/contributors/pystardust/ytfzf?style=flat-square"></a>
	<img src="https://img.shields.io/static/v1?color=%231831ad&message=Euro20179&label=Maintainer&style=flat-square" alt="Maintainer: Euro20179">
	<a href="https://github.com/pystardust/ytfzf/releases/tag/v1.1.1"><img src="https://img.shields.io/github/v/tag/pystardust/ytfzf?style=flat-square"> </a>
	<a href="https://github.com/pystardust/ytfzf/commits/master"><img src="https://img.shields.io/github/commit-activity/m/pystardust/ytfzf?color=green&style=flat-square"></a>
	<a href="https://discord.gg/kupWznHjRJ"><img src="https://img.shields.io/discord/815609275644117022?color=yellow&logo=discord&style=flat-square" alt="Discord"></a>
	<a href="https://matrix.to/#/#ytfzf-chat:matrix.org"><img src="https://img.shields.io/static/v1?color=%230eb687&message=chat&logo=matrix&label=matrix&style=flat-square" alt="Discord"></a>
    <br />
    <br />
    <i>Aaa POSIX script that helps you find Youtube videos (without API) and opens/downloads them using mpv/youtube-dl</i>
	<hr>
</p>

<h1 align="center">
	This is a little showcase..
</h1>
<p align="center">
<img src=.assets/ytfzf.gif width="100%">
</p>

---

# Table Of Contents

* [`Dependencies`](#Dependencies)
* [`Install`](#Install)
* [`Features`](#Features)
* [`Examples`](#Examples)
* [`Todo`](#Todo)
* [`Bugs`](#Bugs)
* [`Credits`](#Credits)

---

# Dependencies

There are only 2 required dependencies, however the rest require some configuration before you can replace them.

## Requried dependencies

* [`jq`](https://github.com/stedolan/jq)
* [`curl`](https://github.com/curl/curl)

## Recommended dependencies

* [`mpv`](https://github.com/mpv-player/mpv) (the default video and audio player)
* [`fzf`](https://github.com/junegunn/fzf) (the default menu selection screen)

## Optional dependencies

* [`yt-dlp`](https://github.com/yt-dlp/yt-dlp) (for downloading)
* [`dmenu`](https://tools.suckless.org/dmenu/) (only if using the -D option)
* [`ueberzug`](https://github.com/seebye/ueberzug) (if using thumbnails (-t) on x11)
    * If on wayland, or you do not want `ueberzug`, see the alternatives [below](#Alternative-Thumbnail-Viewers).
    * To use an alternative include `--thumb-viewer=<alternative>` in the command when running ytfzf

### Alternative Thumbnail Viewers
| Program                                                                           | Wayland Support  |
| :--                                                                               | :--              |
| [`chafa`](https://github.com/hpjansson/chafa)                                     | &#9989;          |
| [`catimg`](https://github.com/posva/catimg)                                       | &#9989;          |
| [`w3m`](https://github.com/tats/w3m) (buggy)                                      | &#10060;         |
| [`imv`](https://git.sr.ht/~exec64/imv)                                            | &#9989;          |
| [`kitty`](https://github.com/kovidgoyal/kitty)                                    | &#9989;          |

# Install

<a href="https://repology.org/metapackage/ytfzf">
    <img src="https://repology.org/badge/vertical-allrepos/ytfzf.svg" alt="Repo status" align="right">
</a>

**if on `linux` and installed using make on version `2.0` or prior, run `sudo make uninstall-old` first**

1. Install the dependencies listed [above](#Dependencies)
2. Run the following commands
```sh
git clone https://github.com/pystardust/ytfzf
cd ytfzf
sudo make install doc
```

* If you wish to not install documentation (highly unrecommended) run `sudo make install` instead.

* You may also install `ytfzf` through your package manager, as listed on the side.

## Addons

Addons are extra features that will not be as supported as everything built into `ytfzf` itself.

Addons are located in `addons`, copy any addon to `~/.config/ytfzf/{addon-type}/{addon}`, and give it execute permissions.

You may also just copy the entire addon folder type, eg: `cp -r addons/thumbnail-viewers ~/.config/ytfzf/`

### Usage

To use a scraper addon run `ytfzf -c <scraper> ...`

To use a thumbnail-viewer addon run `ytfzf --thumb-viewer=<viewer> ...`

To use a interface addon run `ytfzf --interface=<interface> ...`

To use a url-handler addon run `ytfzf --url-handler=<handler> ...`

To use a sort-name addon run `ytfzf --sort-name=<sort-name> ...`

---

# Features

* Subscriptions
* Thumbnails
* Watch history
* Downloading
* Queueing multiple videos

---

# Examples

> Search with thumbnails

```sh
ytfzf -t <search>
```

> Use `dmenu` as the menu instead of `fzf`

```sh
ytfzf -D <search>
```

> Print the link of the selected video instead of playing it

```sh
ytfzf -L <search>
```

> Search Odysee instead of youtube

```sh
ytfzf -cO <search>
```

---
---

# Bugs

* *dwm with swallow patch: Images don't render with ueberzug when looped (ie, option `-l`)*
* *if thumbnails are not working `.Xauthority` might be causing it. Try deleting it and relogging into your computer.*

# Credits

| User           | Contributions                             | Donate|
| :---           | :---                                      | :--- |
| Pystardust    | [contributions](credits/pystardust.md)    ||
| Euro20179     | [contributions](credits/euro20179.md)     | [donate](credits/euro20179.md#Donate) |
| Simonhughxyz  | [contributions](credits/simonhughxyz.md)  ||
| Jac-Zac       | [contributions](credits/jac-zac.md)       ||
| Mudskipper875 | [contributions](credits/mudskipper875.md) ||
