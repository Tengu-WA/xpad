## Xbox One Controllers
This driver is only used if you connect the controller via USB.

**Connecting via Bluetooth**  
If you get past the pairing issues, the controller will operate in the [generic-HID bluetooth profile](https://en.wikipedia.org/wiki/List_of_Bluetooth_profiles#Human_Interface_Device_Profile_(HID)).  
The xpad driver will not be used.

**Connecting via XBox One Wireless Adapter (WiFi)**  
The adapter needs daemon in userspace, see: [medusalix/xow](https://github.com/medusalix/xow)  
Opinion: rather get a controller that supports bluetooth.


# Installing
```
sudo git clone https://github.com/paroj/xpad.git /usr/src/xpad-0.4
sudo dkms install -m xpad -v 0.4
```
# Updating
```
cd /usr/src/xpad-0.4
sudo git fetch
sudo git checkout origin/master
sudo dkms remove -m xpad -v 0.4 --all
sudo dkms install -m xpad -v 0.4
```
# Removing
```
sudo dkms remove -m xpad -v 0.4 --all
sudo rm -rf /usr/src/xpad-0.4
```
