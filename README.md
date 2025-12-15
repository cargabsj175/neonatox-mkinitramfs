 [![License: GPLv3+](https://img.shields.io/badge/license-GPLv3%2B-blue.svg)](LICENSE)[![Language: Bash](https://img.shields.io/badge/language-Bash-green.svg)](https://www.gnu.org/software/bash/)[![Build system: Meson](https://img.shields.io/badge/build-Meson-orange.svg)](https://mesonbuild.com/)[![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/cargabsj175/neonatox-mkinitramfs)

mkinitramfs
===========

mkinitramfs is a simple and transparent initramfs generator, designed following the Linux From Scratch (BLFS) philosophy. It avoids heavy automation and generates a predictable, fully controlled initramfs image.

Origin
------

This project is based on the BLFS documentation:

[https://www.linuxfromscratch.org/blfs/view/systemd/postlfs/initramfs.html](https://www.linuxfromscratch.org/blfs/view/systemd/postlfs/initramfs.html)

Installed files
---------------

*   `/usr/sbin/mkinitramfs` – initramfs generator script
*   `/usr/share/mkinitramfs/init.in` – init script used inside the initramfs

Dependencies
------------

Required at runtime:

*   **cpio** – mandatory

Optional (only if the root filesystem requires them):

*   **LVM2 >= 2.03.37**
*   **mdadm >= 4.4**

Instalation
------------
```
  meson setup builddir --prefix=/usr
  ninja -C builddir
  sudo ninja -C builddir install
```

Notes
-----

This mkinitramfs implementation is intentionally minimal. Only the components strictly required to mount the root filesystem are included.
