Axel’s Metapackages
===================

History
-------

For
[my desktop setup](https://github.com/xtaran/ratpoison-desktop#readme)
I started maintaining metapackages which constitute the packaged
dependencies of the setup.

After a while the list of metapackages started to contain other stuff
which had no direct relation to the desktop setup anymore and most
desktop setup commits affected unrelated metapackages rather than the
desktop setup itself. So I decided to split the git repository up into
two repositories.

Packages
--------

The repository contains source code for the following packages:

### abe-archive-tools

Commandline tools which are needed to handle exotic archive file
formats.

### abe-commandline

Commandline tools I usually want on all my boxes. Its hard
dependencies are also suitable for servers.

### abe-commandline-local

Packages I usually install on all those machines where I log into
locally, i.e. real hardware where I have physical access.

### abe-commandline-media

Commandline tools I usually want for playing audio or video files.

### abe-console

Packages I usually want to have installed on boxes where I have local
console access like laptops, desktops, etc. In other words, it's not
needed on most virtual machines or rented root servers.

### abe-desktop-extras

Packages which I usually want on all my desktops but which are not
needed by
[my desktop setup](https://github.com/xtaran/ratpoison-desktop#readme).

### abe-emacs

Emacs modes and other Emacs add-ons I usually want on all boxes where
I install GNU Emacs anyway.

### abe-fun

Packages which I just install for fun (joke packages, fortune cookies,
etc.).

### abe-games

Recommends or suggests games in Debian I like.

### abe-gnome

GUI tools and applications I usually install if some GNOME
dependencies are ok.

### abe-joystick

Depends on, recommends and suggests packages which help to make
joysticks working.

### abe-laptop

Packages I commonly need on laptops and netbooks. ACPI stuff, resource
saving and monitoring stuff, …

### abe-laptop-ubuntu

Satisfies some of ubuntu-minimal’s annoying hard dependencies to be
able to e.g. install a different syslog daemon without removing the
ubuntu-minimal metapackage.

### abe-monitoring

Pulls in everything I need on machines I want to have monitored (using
[Xymon](http://www.xymon.com/) formerly known as Hobbit).

### abe-office

Depends on the LibreOffice and Gnome Office applications I prefer.

### abe-packaging-dev

Packages I usually need to work on packaging.

### abe-partitioning

Depends on tools I prefer to partition USB sticks or disks, stuff for
disaster recovery of disks or for forensic analysis of disks. Usually
not needed inside virtual machines.

### abe-perl-dev

Packages I usually need to work on Perl modules and scripts.

### abe-server

Taking care that all packages I want to have installed on my servers
are installed and those I don't want to be installed, aren't.

This package especially takes care that there's no dbus, policykit,
consolekit, networkmanager or systemd installed.

### abe-small-disk

Conflicts with packages I consider a waste of disk space, at least if
disk space is sacre. It also pulls in some small packages which help
to find local waste of disk-space.

### abe-tablet

Depends on packages necessary to get a Wacom graphics tablet or a
touchscreen working.

### abe-tex

Depends on packages I prefer on computers where I want to use TeX or
LaTeX.

### abe-text-browsers

Text-mode web browsers, I commonly have installed.

### abe-window-managers

Depends on a bunch of (mostly exotic) window managers and desktop
environments, I want to have on those computers where occassionally
other people log in, too.

### abe-x-browsers

Graphical web browsers for X, I commonly have installed.

### kiva-base

Everything needed on the Dom0 and all DomUs of the
[LUGS](http://www.lugs.ch/lugs/) server "kiva".

### kiva-users

Everything needed on all DomUs of the
[LUGS](http://www.lugs.ch/lugs/) server "kiva" where normal users can
login via SSH.

APT Repository
--------------

All those metapackages are usually also available from
[my APT repository](http://noone.org/apt/).
