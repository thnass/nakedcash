
Debian
====================
This directory contains files used to package nakedcashd/nakedcash-qt
for Debian-based Linux systems. If you compile nakedcashd/nakedcash-qt yourself, there are some useful files here.

## nakedcash: URI support ##


nakedcash-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install nakedcash-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your nakedcashqt binary to `/usr/bin`
and the `../../share/pixmaps/nakedcash128.png` to `/usr/share/pixmaps`

nakedcash-qt.protocol (KDE)

