# Installing and running cockpit on Arch linux for arm on a raspberry Pi


![](/pics/cockpit.png)

In short:
* Get and install pcp from aur.
* Get and install cockpit from aur.

## Prep

Both pcp and cockpit will be built from source so install the necessary tools

``` bash
$ sudo pacman -S base-devel git neovim

```

## pcp

``` bash
$ git clone https://aur.archlinux.org/pcp.git
```

Trim out failed dependencies from PKGBUILD that does not seem to matter:

``` bash
makedepends=(git intltool gtk-doc gobject-introspection networkmanager libgsystem xmlto npm tar) 
```

``` bash
# makepkg -sir
```

This takes a afternoon to compile on an old raspberry pi 

## cockpit

clone cockpit from aur and build. It builds without issue.


``` bash
# systemctl enable cockpit.socket
# systemctl start cockpit.socket
```


