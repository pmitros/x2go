x2go is a project to develop a low-cost platform for use of edX in
off-line settings.

Installing Open edX on the Intel NUC:

* Step 1: [Configure the BIOS](https://www.intel.com/content/www/us/en/support/boards-and-kits/000022600.html)
* Step 2: Download [Ubuntu 16.04 64 bit server](http://releases.ubuntu.com/16.04/). dd it to a USB stick, and install it
* Step 3: Install [Open edX](https://openedx.atlassian.net/wiki/display/OpenOPS/Native+Open+edX+Ubuntu+16.04+64+bit+Installation)
* Step 4: Install extra configuration from x2go configuration `/ansible-playbook local.yml -i '127.0.0.1,' -c local -e`
* Step 5: Create an account (via web interface), and make it into an active superuser:

     #mysql
     use edxapp
     update auth_user set is_active=1, is_staff=1, is_superuser=1 where username='pmitros';

* Step 6: Install x2go packages
* Step 7: Load courses

This project has been through a few reboots. See version history if
you care.