Axel's Tiling Window Manager Setup
==================================

History, Background and Reasoning
---------------------------------

While being a heavy FVWM user for nearly 15 years, I now run tiling
window managers on all my "desktops" and laptops, ranging from a first
generation ASUS EeePC 701 4G netbook over a Sun UltraSparc 10 to a
full-fledged multihead workstation from Dalco at work.

My ASUS EeePC 701 running Debian GNU/Linux Sid was the first box where
I did not use FVWM anymore, because with a resolution of 800x480 on a
7 inch screen, you a) want to waste as few pixels as possible by title
bars, borders, etc. and b) most of the time anything else than
fullscreen windows doesn't make sense, moving windows around with the
mouse makes even less sense.

So I've chosen ratpoison for the EeePC (and still use it on that box)
since it makes windows fullscreen by default and the keybindings are
nearly identical to GNU Screen and therefore easy to learn
respectively I didn't have to learn anything to use it.

After more and more fine tuning involving the xmobar text status bar,
filled with data by i3status, I started this git repository to track
my own changes, to share the setup with some other of my boxes (like
the UltraSparc or my bed-side terminal, an older ThinkPad A31).

Getting used with a fullscreen and tiling setup on the EeePC I more
and more wanted something for my everyday ThinkPad T61, too. But while
ratpoison is really perfect for the small EeePC screen, it proved too
clumsy for more complex window arrangements and multiple virtual
desktops.

So I looked through the other tiling window managers in Debian, trying
out i3, spectrwm (formerly scrotwm), wmii and awesome and some ion
successors (tritium and anion). I finally stuck with awesome, first
the 2.x version from Debian 5.0 Lenny, now the 3.x version from Debian
6.0 Squeeze.

In general I liked the idea of using the -- on Linux mostly unused --
Windows key as window manager meta key. I even configured my ratpoison
to use that in addition to the original Ctrl-T prefix.

You will also find some configuration for i3 (version 4 and upwards)
in the repo as I also experiment with i3's tree-based layout to see if
I can workaround some of awesome's shortcomings by using i3 instead.


Repository Name and URLs
------------------------

So this repository is no more a ratpoison only setup. But since I
neither want to change the repository name nor any URL I decided that
I stick with having "ratpoison" in the name. The amount of "rodent"
usage you need with this setup hasn't changed anyway, so without the
relation to the window manager of this name, the name is still fitting
(as it fits to the window manager of that name :-).


Installation
------------

These files are needed to get the setup running. The setup currently
runs on Debian Sid and Squeeze as well as Ubuntu Natty. It probably
also runs on older Ubuntu releases.

Since most of the configuration files included are not expected to
reside in .ratpoison, some symlinks are necessary where config file
paths cannot be set via command line options or where it would be to
tedious to always type them:

    ~/.gitconfig   → gitconfig
    ~/.xsession    → xsession
    ~/.screenrc    → screenrc
    ~/.colordiffrc → colordiffrc

These symbolic links can also be automatically setup by calling
bin/setup-symlinks.sh from this repository.

Sources available via http://git.noone.org/?p=ratpoison.git,
http://gitorious.org/abe/ratpoison-desktop, and
http://github.com/xtaran/ratpoison-desktop.

Requirements
------------

### Required Software Packages

Needs at least the following Debian packages (besides essential
packages) to be installed:

* busybox-syslogd (for logread)
* conkeror or some other web browser
* emacs (or emacsen, for emacs and emacsclient)
* gnome-keyring (for gnome-settings-daemon)
* hsetroot
* i3status >= 2.2
* libfile-slurp-perl
* libfile-temp-perl
* lsb-release
* ratmenu >= 2.3.20
* ratpoison or awesome + awesome-extra
* wget (needed by iplet)
* x11-utils (for xmessage) or gxmessage
* x11-xserver-utils (for xmodmap, xrdb, xrandr and xsetroot)
* xmobar
* xscreensaver or xtrlock
* xterm and/or rxvt-unicode
* For Focus-Follows-Mouse:
  * for awesome: xdotool
  * for ratpoison: xdotool or nawm (no more in Debian)

The project's subdirectory `abe-desktop` contains a Debian source
package which can generate a few metapackage .debs which (should)
contain all the mentioned dependencies. They're usually also available
via APT from my APT repository at http://noone.org/apt/.

### Used Fonts

Fonts used for xmobar:

* ttf-mplus | fonts-mplus
* ttf-droid | fonts-droid
* xfonts-terminus

### Optional Software Packages

Used if available but except the system tray stuff recommended anyway:

* autocutsel
* inotail
* keynav >= 0.20101014.3067
* redshift
* unclutter
* x11-xkb-utils (for setxkbmap)
* xrootconsole
* xserver-xorg-input-synaptics (for synclient+syndaemon)
* yeahconsole
* System tray applets for use with awesome:
  * nm-applet
  * wicd-gtk
  * update-notifier
  * gtk-redshift
  * fdpowermon
  * radiotray
  * shutter
  * yarssr
  * qasmixer | volumeicon-alsa

### Kernel Modules

Linux kernel modules which may be used by some features of xmobar, but
do not seem to be loaded automatically (write them into /etc/modules):

* acpi_cpufreq
* coretemp

### Software Packages used by Scripts or Keybindings

Only used in non-necessary scripts or keybindings:

* dwm-tools >= 31-1 or suckless-tools (for dmenu, tabbed and wmname)
* openssh-client (for ssh-add and ssh-agent)
* screen
* scrot
* transset-df
* xclip
* colordiff

### Software Packages used in Commented Code

Only in commented code (i.e. currently not used):

* Alternative window and session managers:
  * i3
  * flwm
  * fvwm
  * lxsession
  * spectrwm (formerly scrotwm)
  * stumpwm
  * tritium (or not yet packaged: anion3 and notion)
* loco, ccze, lwatch, or colortail
* root-tail
* xcompmgr