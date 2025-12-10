stx is a unified package manager wrapper for Arch Linux.  
It provides a single command to acquire (install) or purge (remove) software across multiple ecosystems, including:

- `pacman` (official Arch repositories)
- `yay` / `paru` (AUR helpers)
- `flatpak`
- `snap`
- `git` (source repositories)
- `pip` (Python packages)
- `npm` (Node.js packages)
- `cargo` (Rust crates)

---
Features

- One command for all major package managers.
- Automatically detects which service can provide the requested package.
- Modular design: easy to add new services.
- Consistent syntax for install/remove operations.

---
Installation

1. Clone the repository:
   git clone https://github.com/yourusername/stx.git
   cd stx
2. Make the script executable:
  chmod +x stx
3. Move it into your $PATH (e.g., /usr/local/bin):
   sudo mv stx /usr/local/bin/

---
Usage

Acquire (install)

sudo stx acquire firefox
sudo stx acquire numpy
sudo stx acquire vlc

Purge (remove)

sudo stx purge firefox
sudo stx purge numpy
sudo stx purge vlc

---
Configuration

The order of services is defined in the script (SERVICES=(pacman yay paru flatpak snap git pip npm cargo)).

You can reorder or remove services depending on your preference.

Add new services by defining acquire_service and purge_service functions.

---
Notes

sudo is required for system-level package managers (pacman, yay, paru, snap).

User-level managers (pip, npm, cargo) may not require sudo depending on your environment.

Git installs are cloned into /opt/<package> by default.

---

Please report any errors or issues
