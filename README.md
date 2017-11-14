# Modified Wifite for WiFi Pineapple NANO + TETRA

Discontinued, [discussion thread](https://forums.hak5.org/topic/40108-wifi-pineapple-wifite/)

## Getting Started

SSH to your Pineapple. Launch the INSTALL.sh script to install Wifite.

### Installing

```bash
wget -qO- https://raw.githubusercontent.com/kbeflo/wifite-openwrt/master/INSTALL.sh | bash
```

## Running Wifite

```bash
wifite-ng

wifite-ng --help
```

Modified version of https://github.com/aanarchyy/wifite-mod-pixiewps to include some fixes:

* Fixes for tshark from https://github.com/darkr4y/wifite-mod
* Macchanger fix
* Oui lookup for pingen attack

### Added flags
    -pto <sec>        # configurable timeout for pixiewps attack, default 660
    -ponly            # uses only pixiewps and reaver up until M3
    -pnopsk           # do not run retrieved pin through reaver
    -paddto <sec>     # add n seconds to timeout on each hash retrevial, default 30
    -update           # now updates to this fork instead of original wifite
    -endless          # will now loop through targets forever until stopped

### ToDo
    Add check for pixiewps, modified reaver, and offer option to install.
    Add check to see if update is needed before performing.
    Add option to dynamically spoof connected client while running attack.
    Add option to auto-skip previously cracked AP instead of prompting.
    Add recording for individual access points(clients, signal strength, hashes, solved pins, etc).

#### May do    
    Add option to download and install pixiewps and modified reaver from github
    Add mdk3 support
    Add default pin calculations and options

## Acknowledgements

* Thanks to the authors of wifite-ng! Forked from https://github.com/binkybear/wifite-mod-pixiewps
* Many thanks for the help and guidance: Andreas Nilsen - https://www.github.com/adde88

---

Distributed under the GNU GENERAL PUBLIC LICENSE v3. See [LICENSE](https://github.com/kbeflo/wifite-openwrt/blob/master/LICENSE) for more information.

Note that this repo is for educational purposes only. No contributors, major or minor, are to fault for any actions done by this program.

Kleo Bercero - [@kbeflo](https://twitter.com/kbeflo) - [My website](https://kerberos.me/)

Support me on - [Patreon](https://www.patreon.com/kbeflo)
