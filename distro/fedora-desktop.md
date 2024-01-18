# Fedora

## Upgrade the system

1. To update your Fedora release from the command-line do:

   `sudo dnf upgrade --refresh`

   and reboot your computer.

2. Install the dnf-plugin-system-upgrade package if it is not currently installed:

   `sudo dnf install dnf-plugin-system-upgrade`

3. Download the updated packages:

   `sudo dnf system-upgrade download --releasever=39`

4. Trigger the upgrade process. This will reboot your machine (immediately!, without a countdown or confirmation, so close other programs and save your work) into the upgrade process running in a console terminal:

   `sudo dnf system-upgrade reboot`

## Enable Third-Party Repositories if You Didn't

### ENABLE RPMFUSION

`sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm`

`sudo dnf --refresh upgrade`

`sudo dnf groupupdate core`

## Multimedia

### SWITCH TO FULL FFMPEG

`sudo dnf swap ffmpeg-free ffmpeg --allowerasing`

### INSTALL ADDITIONAL CODEC

`sudo dnf install gstreamer1-plugins-{bad-\*,good-\*,base} gstreamer1-plugin-openh264 gstreamer1-libav --exclude=gstreamer1-plugins-bad-free-devel`

`sudo dnf install lame\* --exclude=lame-devel`

`sudo dnf group upgrade --with-optional Multimedia`

## Hardware acceleration

### INTEL

#### Intel(recent) Using the rpmfusion-nonfree section

`sudo dnf install intel-media-driver`

#### Intel(older) Using the rpmfusion-free section

`sudo dnf install libva-intel-driver`

### AMD

`sudo dnf swap mesa-va-drivers mesa-va-drivers-freeworld`

`sudo dnf swap mesa-vdpau-drivers mesa-vdpau-drivers-freeworld`

## Microsoft Fonts on Fedora

`sudo dnf install curl cabextract xorg-x11-font-utils fontconfig`

`sudo rpm -i https://downloads.sourceforge.net/project/mscorefonts2/rpms/msttcore-fonts-installer-2.6-1.noarch.rpm`

### check

`fc-match TimesNewRoman`

## RAR Files

`sudo dnf install unrar`
