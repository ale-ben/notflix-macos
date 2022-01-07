[![CodeFactor](https://www.codefactor.io/repository/github/ale-ben/notflix-macos/badge)](https://www.codefactor.io/repository/github/ale-ben/notflix-macos)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/356f544150d048588d58d08e7ca582cb)](https://www.codacy.com/gh/ale-ben/notflix-macos/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=ale-ben/notflix-macos&amp;utm_campaign=Badge_Grade)
[![Codiga Code Grade](https://api.codiga.io/project/30640/status/svg)](https://app.codiga.io/public/project/30640/notflix-macos/dashboard)
[![Codiga Code Quality Score](https://api.codiga.io/project/30640/score/svg)](https://app.codiga.io/public/project/30640/notflix-macos/dashboard)
<h1 align="center">NOTFLIX MacOS</h1>
<p align="center">f@#k netflix use notflix a tool which search magnet links and stream it with webtorrent</p>

## This is a fork of Bugswriter/notflix
The original project is [Bugswriter/notflix](https://github.com/Bugswriter/notflix).

This is a version made to be compatible with MacOS.
### Differences
- Replaced dmenu with command line input, less beautifull but compatible
- Replaced notify-send with terminal-notifier
- Replaced grep -P
- Updated 1337x address

> Watch my video on this - [bugswriter's notflix](https://youtu.be/RFJCL9C46Mc)

### How does this work?

This is a shell script. It scrapes 1337x and gets the magnet link.
After this it uses [webtorrent](https://webtorrent.io/) to stream the video from the magnet link.
For scraping, the script uses simple gnu utils like sed, awk, paste, cut.

## Requirements

* [nodeJS](https://nodejs.org/en/) > 12.20
* [webtorrent](https://webtorrent.io/) - A tool to stream torrent. `npm install webtorrent-cli -g`
* [OPTIONAL][Terminal Notifier](https://formulae.brew.sh/formula/terminal-notifier) - A tool to crerate notifications from terminal `brew install terminal-notifier`

## Installation

### cURL
cURL **notflix** to your **$PATH** and give execute permissions.

```sh
$ sudo curl -sL "https://raw.githubusercontent.com/Bugswriter/notflix/master/notflix" -o /usr/local/bin/notflix
$ sudo chmod +x /usr/local/bin/notflix
```
- To update, just do `curl` again, no need to `chmod` anymore.
- To uninstall, simply remove `notflix` from your **$PATH**, for example `sudo rm -f /usr/local/bin/notflix.

## License
This project is licensed under [GPL-3.0](https://raw.githubusercontent.com/Illumina/licenses/master/gpl-3.0.txt).

