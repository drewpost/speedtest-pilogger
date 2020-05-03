# speedtest-pilogger
Use the official Speedtest CLI to record your download, upload and latency measurements on your Raspberry Pi

Tested against a RaspberryPi 4 B running Raspbian Buster

Step 1: Download and install the official Speedtest.net command line tester for Debian

```
sudo apt-get install gnupg1 apt-transport-https dirmngr
export INSTALL_KEY=379CE192D401AB61
export DEB_DISTRO=$(lsb_release -sc)
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys $INSTALL_KEY
echo "deb https://ookla.bintray.com/debian ${DEB_DISTRO} main" | sudo tee  /etc/apt/sources.list.d/speedtest.list
sudo apt-get update
```

Using non official binaries like speedtest-cli will result in a conflict. Make sure to uninstall any before proceeding with this. 
