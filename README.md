# Custom MacPorts Repository

## Setup

Add the following line above `rsync://...` in `/opt/local/etc/macports/sources.conf`:

file:///opt/local/myports

## Install

```bash
sudo mkdir -p /opt/local/myports
curl -fsSL https://github.com/htrb/macports/releases/download/latest/ports.tar.gz | sudo tar -xzf - -C /opt/local/myports
sudo port sync
sudo port install ngraph-gtk-devel
```
