# Custom MacPorts Repository (ngraph-gtk-devel)

A custom MacPorts repository providing `ngraph-gtk-devel`.

## Prerequisites

* macOS
* [MacPorts](https://macports.org) installed

## Setup (First-Time Only)

To make the ports in this repository available, add this repository to your MacPorts sources list.

### 1. Clone the Repository

Clone this repository to a local directory of your choice (e.g., `/opt/local/share/macports-local/ngraph`):

```bash
sudo git clone https://github.com/htrb/macports.git /opt/local/share/macports-local/ngraph
```

### 2. Register in `sources.conf`

Open `/opt/local/etc/macports/sources.conf` with root privileges and add the local path **above** the default `rsync://...` entry:

```bash
sudo vi /opt/local/etc/macports/sources.conf
```

**Example:**

```text
file:///opt/local/share/macports-local/ngraph
rsync://rsync.macports.org/macports/release/tarballs/ports.tar [default]
```

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
sudo git -C /opt/local/share/macports-local/ngraph pull
sudo port sync
sudo port upgrade ngraph-gtk-devel
```

## Uninstallation

To uninstall the port:

```bash
sudo port uninstall ngraph-gtk-devel
```

To completely remove this repository, delete the `file://...` line from `/opt/local/etc/macports/sources.conf` and remove the cloned directory.
