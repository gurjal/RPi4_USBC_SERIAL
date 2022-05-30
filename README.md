# RPi4_USBC_SERIAL
Credit: hardill.me.uk/wordpress/2019/11/02/pi4-usb-c-gadget/

'setup' executes the following instructions from the working directory

- Add 'dtoverlay=dwc2' to the /boot/config.txt

- Add 'modules-load=dwc2' to the end of /boot/cmdline.txt

- If you have not already enabled ssh then create a empty file called 'ssh' in /boot

- Add 'libcomposite' to /etc/modules

- Add 'denyinterfaces usb0' to the top of /etc/dhcpcd.conf

- Install dnsmasq with 'sudo apt-get install dnsmasq'

- Move the following files to the specified locations:
    usb -> /etc/dnsmasq.d/usb
    usb0 -> /etc/network/interfaces.d/usb0
    usb.sh -> /root/usb.sh

- Make /root/usb.sh executable with 'chmod +x /root/usb.sh'

- Add /root/usb.sh to /etc/rc.local before 'exit 0'

ssh {user}@10.55.0.1
