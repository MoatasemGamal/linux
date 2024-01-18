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
