# README #

### What is this repository for? ###

The script should run on a mac or linux system.

### What do you need? ###

This script requires the following programs to be installed on the system (and it will check for them and report if it cannot find them):
* curl
* resty (provided in this repo)
* jq version 1.4 (probably needs to be installed or even build from source and installed)

### How do I install/run it? ###

To install/run the icon_reboot script, just create a directory, copy the two files from this repository (icon_reboot and resty) into that directory, then type ./icon_reboot to get more info.

The normal usage is shown below and show show on your screen when you type in the command above:

Usage: icon_reboot [options] IP [IP ...]
  Options/Arguments:
   -n        run the script, but do NOT do the actual reboot, just report.
   -p pass   provide the admin password on the commandline.
   -d        enable debug mode
   IP        IP address (or DNS name) of Lifesize Icon. You can have
             one or more IP addresses on the command line.

NOTE:
  The easiest way to provide the list of IP addresses is to put them in a
  text file and then use the text file like this on the command line:
  icon_reboot $(cat FILE_OF_IP_ADDRESSES)

If you want to test it out just do this:

./icon_reboot -n IPADDR_OF_YOUR_ICON

This will do the tests for:
- do I have all the programs I need
- is it in a call
- is it doing an upgrade
- then it will just tell you that it would have rebooted it, but won’t actually do the reboot


### Who do I talk to? ###

* Mike Burkett -- mike@burkett.org