# google chrome problems

## locked profile (The profile appears to be in use)

> Google Chrome - The profile appears to be in use by another Google Chrome process ({process-number}) on another computer ({linux-distribution-name}). Chrome has locked the profile so that it doesn't get corrupted. If you are sure no other processes are using this profile, you can unlock the profile and relaunch Chrome.

### Solution, try:

_remove lock file on each kiosk using SSH (PK Server has an option to execute a command on the client side):_

` rm ~/.config/google-chrome/SingletonLock`

`rm -rf ~/.config/google-chrome/Singleton* `

`rm -rf /tmp/.config/chromium/Singleton*`

### Resources:

[Google Chrome locked profile](https://forum.porteus.org/viewtopic.php?t=8835)

[Google Chrome wont start after changing hostname](https://askubuntu.com/questions/476918/google-chrome-wont-start-after-changing-hostname)
