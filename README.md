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
---------

The repository contains source code for the following packages:

* abe-commandline: Commandline tools I usually use. Its hard
  dependencies are also suitable for servers.
* abe-emacs: Emacs modes and other Emacs add-ons I usually want on all
  boxes where I install GNU Emacs anyway.
* abe-gnome: GUI tools and applications I usually install if some
  GNOME dependencies are ok.
* abe-office: Depends on the LibreOffice/GnomeOffice applications I
  prefer.
* abe-laptop: Packages I commonly need on laptops and netbooks. ACPI
  stuff, resource saving and monitoring stuff, … Also satisfies some
  of ubuntu-minimal’s hard dependencies to be able to e.g. install a
  different syslog daemon without removing the metapackage.
* ...

### APT Repository

All those metapackages are usually also available from
[my APT repository](http://noone.org/apt/).
