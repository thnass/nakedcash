
Debian
====================
This directory contains files used to package nakedcashd/Nakedcash-qt
for Debian-based Linux systems. If you compile nakedcashd/Nakedcash-qt yourself, there are some useful files here.

## Nakedcash: URI support ##


Nakedcash-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install Nakedcash-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your Nakedcashqt binary to `/usr/bin`
and the `../../share/pixmaps/Nakedcash128.png` to `/usr/share/pixmaps`

Nakedcash-qt.protocol (KDE)

