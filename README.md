# ufetch

> This is an unofficial fork, the original can be found [here](https://gitlab.com/jschx/ufetch).

ufetch is a tiny system information display tool for Unix-like operating systems.

![ufetch](https://jschx.gitlab.io/images/ufetch.png)

## Supported Systems

Here's a list of all currently supported systems with an ASCII logo:

- [Alpine](https://alpinelinux.org/)
- [Android](https://www.android.com/) **[REMAKE NEEDED]**
- [Antergos](https://distrowatch.com/antergos)
- [Arch](https://archlinux.org/)
- [Archbang](https://archbang.org/)
- [Arco](https://www.arcolinux.info/)
- [Artix](https://artixlinux.org/)
- A/UX
- [CentOS](https://www.centos.org/)
- [Crux](https://crux.nu/)
- [Debian](https://www.debian.org/)
- [Devuan](https://www.devuan.org/)
- [ElementaryOS](https://elementary.io/)
- [Fedora](https://fedoraproject.org/)
- [FreeBSD](https://www.freebsd.org/)
- [Gentoo](https://www.gentoo.org/)
- [gNewSense](https://distrowatch.com/gNewSense)
- [GNU Guix](https://guix.gnu.org/)
- [Hyperbola](https://www.hyperbola.info/)
- [IstantOS](https://instantos.io/)
- Linux (General Logo)
- [Linux Lite](https://www.linuxliteos.com/)
- [MacOS](https://www.apple.com/macos/sonoma/)
- [Mageia](https://www.mageia.org)
- [Manjaro](https://manjaro.org/)
- [Linux Mint](https://linuxmint.com/)
- [MX Linux](https://mxlinux.org/)
- [NetBSD](https://www.netbsd.org/)
- [NixOS](https://nixos.org/)
- [OpenBSD](https://www.openbsd.org/)
- [Parabola](https://www.parabola.nu/)
- [Pop!_OS](https://pop.system76.com/)
- [PureOS](https://www.pureos.net/)
- [RaspberryPiOS](https://www.raspberrypi.com/software/)
- [ReactOS](https://reactos.org/) **[REMAKE NEEDED]**
- [Rocky](https://rockylinux.org/) **[REMAKE NEEDED]**
- [Slackware](http://www.slackware.com/)
- [openSUSE](https://www.opensuse.org/)
- [Ubuntu](https://ubuntu.com/)
- [Void](https://voidlinux.org/)
- [Voyager](https://voyagerlive.org/)

## TODO

* [ ] Optimize all scripts [22% done]
* [ ] Add more ASCII logos
* [ ] Fix Android, ReactOS and Rocky Linux
* [ ] Remove dependencies to hostname where possible
* [ ] Reduce package count pipelines where possible
* [ ] Add support for sx in UI detection
* [ ] Add documentation and possibly other **optional** modules

## Optional Modules

```bash
memusage="$(free -h | awk '/^Mem:/{print $3}') / $(free -h | awk '/^Mem:/{print $2}')"
swap="$(free -h | awk '/^Swap:/{print $3}') / $(free -h | awk '/^Swap:/{print $2}')"
date="$(date +"%F")"
hour="$(date +"%H:%M:%S")"
init="$(ps -p 1 -o comm=)"
disk="$(df -h * | awk 'NR==2{print $3" / "$2}')"
browser="$(xdg-settings get default-web-browser | sed 's/\.desktop//g')"
mediaplayer="$(xdg-mime query default audio/mpeg | sed 's/\.desktop//g')"
```

## Info

- Execution Time: ≈ 20 milliseconds **(30 milliseconds faster than the original)**
- Default Modules: Hostname, Kernel, Uptime, Packages, Shell, UI (DE/WM)
- Optional Modules: Memory Usage, Swap Usage, Date, Hour, Init System, Disk Space, Browser, Media Player
- Original Creator: [jschx](https://gitlab.com/jschx)
