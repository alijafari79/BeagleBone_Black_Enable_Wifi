# BeagleBone_Black_Enable_Wifi
BeagleBone Black enable wifi technology through USB port using a usb wifi adaptor



## Check if firmware of usb wifi adapter exists :

```
ls /lib/firmware | grep mt76
```

## Check if wifi is included in connmanctl technologies :

```
connmanctl technologies
```

If nothing shown then :

```
sudo apt update && apt install -y firmware-ralink firmware-misc-nonfree && modprobe mt7601u
```

### Check again :

```
ls /lib/firmware | grep mt76
```

Connect and disconnect the usb wifi adaptor.
Check the log message of devices to ensure that there is no error.

```
dmesg -wH
```

### Install resolve.conf

```
apt install resolvconf
```

```
sudo dpkg-reconfigure resolvconf
```

### Last Check "connmanctl technologies"

```
connmanctl technologies
```

https://youtu.be/PpWjmkTSKYM



### Turn on wifi :

https://youtu.be/wPy0ldR02Is

---

https://linuxconfig.org/etcnetworkinterfacesto-connect-ubuntu-to-a-wireless-network
