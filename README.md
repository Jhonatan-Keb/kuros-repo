# KurOs packages

The pacman repository of KurOs Linux: the desktop, its system parts, the
login and Firefox's theming, rebuilt and signed on every change. Machines
installed from the KurOs ISO update from here with `sudo pacman -Syu`.

The artwork (cursors, wallpapers, element emblems) and the emoji font are not
here: the art is other people's, and comes only with the ISO.

## Using it

In `/etc/pacman.conf`:

```ini
[kuros]
SigLevel = Required
Server = https://jhonatan-keb.github.io/kuros-repo/$arch
```

Every package and the database are signed with the KurOs key, which the
`kuros-keyring` package installs. On a machine that does not have it yet:

```sh
curl -fsSL https://jhonatan-keb.github.io/kuros-repo/kuros.gpg | sudo pacman-key --add -
sudo pacman-key --lsign-key 7FFFDEBE8789645099670DD2E218725F3CC01239
```

Key fingerprint: `7FFF DEBE 8789 6450 9967  0DD2 E218 725F 3CC0 1239`

The packages are built automatically from KurOs's private source repository.
No license is granted for the packaged code: all rights are reserved.
