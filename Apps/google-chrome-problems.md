# google chrome problems

## Table Of Content

1. [locked profile problem](#locked-profile-the-profile-appears-to-be-in-use)
2. [Emojis not displayed](#emojis-not-displayed)

## locked profile (The profile appears to be in use)

> Google Chrome - The profile appears to be in use by another Google Chrome process ({process-number}) on another computer ({linux-distribution-name}). Chrome has locked the profile so that it doesn't get corrupted. If you are sure no other processes are using this profile, you can unlock the profile and relaunch Chrome.

### Solution, try:

_remove lock file on each kiosk using SSH (PK Server has an option to execute a command on the client side):_

` rm ~/.config/google-chrome/SingletonLock`

`rm -rf ~/.config/google-chrome/Singleton* `

`rm -rf /tmp/.config/chromium/Singleton*`

### Resources:

- [Google Chrome locked profile](https://forum.porteus.org/viewtopic.php?t=8835)

- [Google Chrome wont start after changing hostname](https://askubuntu.com/questions/476918/google-chrome-wont-start-after-changing-hostname)

## Emojis not displayed

> emojis displayed as squares

![emojis displayed as squares](../assets/emojis-displayed-as-squares.png)

### Solution:

_install or reinstall fonts-noto-color-emoji or google-noto-emoji-fonts_

1. in Ubuntu

   `sudo apt install fonts-noto-color-emoji`

   `sudo apt reinstall fonts-noto-color-emoji`

2. in Fedora

   `sudo dnf install google-noto-emoji-fonts`

   `sudo dnf reinstall google-noto-emoji-fonts`

### Resources:

- [Why Aren’t Color Emojis Showing Up in Chrome and Firefox on Ubuntu 18.04?](https://devicetests.com/color-emojis-chrome-firefox-ubuntu)

- [How To Enable Color Emoji on Chrome for Linux (Updated)](https://www.omgubuntu.co.uk/2016/08/enable-color-emoji-linux-google-chrome-noto)

- [fedoraproject rpms / google-noto-emoji-fonts](https://src.fedoraproject.org/rpms/google-noto-emoji-fonts)
