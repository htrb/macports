# Custom MacPorts Repository

## Setup

Add the following line above `rsync://...` in `/opt/local/etc/macports/sources.conf`:

https://github.com/htrb/macports/releases/download/latest/ports.tar.gz

## Install

```bash
sudo port selfupdate
sudo port install ngraph-gtk-devel
```
