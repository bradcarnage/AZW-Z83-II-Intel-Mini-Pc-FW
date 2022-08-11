# Z83-1-Intel-Mini-Pc-FW 

        Z83(BZW-BT3)
                        "Stability"


first append to /etc/default/grub GRUB_CMDLINE_LINUX_DEFAULT="intel_idle.max_cstate=0 processor.max_cstate=1 " entries

than regenerate grub config in common way 

or edit manually 

/boot/grub/grub.cfg 

by adding "intel_idle.max_cstate=0 processor.max_cstate=1" entries after vmlinuz (....) root=...

if systemd-boot is installed bootloader edit commandline last entry in any file in 

/boot/efi/loader/entries/*.conf

by adding "intel_idle.max_cstate=0 processor.max_cstate=1"

                              "Bluetooth Installation/Fix"

copy firmware files from this repo to /lib/firmware/brcm/

make copy BCM43341B0.hcd to BCM.hcd in /lib/firmware/brcm/

sudo cp /lib/firmware/brcm/BCM43341B0.hcd /lib/firmware/brcm/BCM.hcd

install package: "bluez-test" (for btmgmt) / on Arch Linux : bluez bluez-tools bluez-utils

opensuse :

sudo zypper in bluez-test


than set to not default bt adapter mac address 

sudo btmgmt -i hci0 public-addr 43:34:1b:00:1a:ac ///for example

bluetooth should be in tray now (tested on blueman-applet)

                        "Hardware codecs"
also install intel-hybrid-driver for vp 8 / 9  vaapi codecs


vainfo repports additionaly


      VAProfileVP9Profile0            :	VAEntrypointVLD'
      
      
      
https://lkml.iu.edu/hypermail/linux/kernel/1904.1/01727.html
      
