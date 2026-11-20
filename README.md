# Custom MacPorts Repository (ngraph-gtk-devel)

A custom MacPorts repository providing `ngraph-gtk-devel`.

## Prerequisites

* macOS
* [MacPorts](https://macports.org) installed

## Setup (First-Time Only)

To make the ports in this repository available, add this repository to your MacPorts sources list.

### 1. Clone the Repository

Clone this repository to a local directory of your choice (e.g., `~/.local/share/macports`):

```bash
git clone https://github.com/htrb/macports.git ~/.local/share/macports
```

### 2. Register in `sources.conf`

Open `/opt/local/etc/macports/sources.conf` with root privileges and add the local path **above** the default `rsync://...` entry:

```bash
sudo vi /opt/local/etc/macports/sources.conf
```

**Example (replace `<your-macos-username>` with your actual macOS username):**

```text
file:///Users/<your-macos-username>/.local/share/macports
rsync://rsync.macports.org/macports/release/tarballs/ports.tar [default]
```

> **Note:** MacPorts does not expand `~` (tilde) in `sources.conf`. Make sure to specify the full path starting with `/Users/<your-macos-username>/...`.

### 3. Sync Port Index

```bash
sudo port sync
```

## Installation

Once the setup is complete, install the port using:

```bash
sudo port install ngraph-gtk-devel
```

## Upgrading

To update to the latest version, pull the latest changes from this repository, sync the index, and upgrade the port:

```bash
git -C ~/.local/share/macports pull
sudo port sync
sudo port upgrade ngraph-gtk-devel
```

## Uninstallation

To uninstall the port:

```bash
sudo port uninstall ngraph-gtk-devel
```

To completely remove this repository, delete the `file://...` line from `/opt/local/etc/macports/sources.conf` and remove the cloned directory.
