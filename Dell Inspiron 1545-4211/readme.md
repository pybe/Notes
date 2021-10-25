# Installing Ubuntu Server 20.04 on Dell Inspiron 1545 Laptop

### Basic setup
Create usb install

F12 on boot and choose USB

Install sees wired networking but not wireless

Select ssh to be installed

Seemed to crash trying to reboot at end. 

After holding power button down ad booting the install everything seems ok.

apt update && apt upgrade

edit /etc/issue to show ip on the login screen.

IP Address: \4
Ubuntu 20.04.3 LTS \n \l

### Get wifi working
lspci
0c:00.0 Network controller: Broadcom Inc. and subsidiaries BCM4312 802.11b/g LP-PHY (rev 01)

apt install bcmwl-kernel-source

Now I have  wlp12s0

created netplan config for it, reboot.

we have a working wifi connection.

Stuck on boot waiting for network, plugged eth back in to boot and added optional: true in netplan for both interfaces.






