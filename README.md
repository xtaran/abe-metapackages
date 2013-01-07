Axel’s Metapackages
===================

History
-------

For my
[desktop setup](https://github.com/xtaran/ratpoison-desktop#readme) I
started maintaining metapackages which constitute the packaged
dependencies of the setup.

After a while the list of metapackages started to contain other stuff
which had no direct relation to the desktop setup anymore and most
desktop setup commits affected unrelated metapackages rather than the
desktop setup itself. So I decided to split the git repository up into
two repositories.

Packages
--------

The repository contains source code for the following packages:

### abe-commandline

Commandline tools I usually want on all my boxes. Its hard
dependencies are also suitable for servers.

### abe-commandline-media

Commandline tools I usually want for playing audio or video files.

### abe-console

Packages I usually want to have installed on boxes where I have local
console access like laptops, desktops, etc. In other words, it's not
needed on most virtual machines or rented root servers.

### abe-emacs

Emacs modes and other Emacs add-ons I usually want on all boxes where
I install GNU Emacs anyway.

### abe-gnome

GUI tools and applications I usually install if some GNOME
dependencies are ok.

### abe-laptop

Packages I commonly need on laptops and netbooks. ACPI stuff, resource
saving and monitoring stuff, …

### abe-laptop-ubuntu

Satisfies some of ubuntu-minimal’s annoying hard dependencies to be
able to e.g. install a different syslog daemon without removing the
ubuntu-minimal metapackage.

### abe-office

Depends on the LibreOffice and Gnome Office applications I prefer.

### abe-partitioning

Depends on tools I prefer to partition USB sticks or disks, stuff for
disaster recovery of disks or for forensic analysis of disks. Usually
not needed inside virtual machines.

### abe-small-disk

Conflicts with packages I consider a waste of disk space, at least if
disk space is sacre. It also pulls in some small packages which help
to find local waste of disk-space.

### abe-window-managers

Depends on a bunch of (mostly exotic) window managers and desktop
environments, I want to have on those computers where occassionally
other people log in, too.

APT Repository
--------------

All those metapackages are usually also available from
[my APT repository](http://noone.org/apt/).
