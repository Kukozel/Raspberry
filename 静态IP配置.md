#Static IP
> - $sudo nano /etc/network/interfaces

```
auto

iface lo inet loopback
#iface eth0 inet dhcp

iface eth0 inet static
address 192.168.2.10
netmask 255.255.255.0
gateway 192.168.2.1

allow-hotplug wlan0
iface wlan0 inet manual
wpa-roam /etc/wpa_supplicant/wpa_supplicant.conf
iface default inet dhcp
``` 
> - $sudo /etc/init.d/networking restart
> - $sudo ifup eth0