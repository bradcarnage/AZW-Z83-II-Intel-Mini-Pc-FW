# Z83-1-Intel-Mini-Pc-FW 

Z83(BZW-BT3)

Bluetooth Installation/Fix:

copy firmware files from this repo to /lib/firmware/brcm/

make copy BCM43341B0.hcd to BCM.hcd in /lib/firmware/brcm/

sudo cp /lib/firmware/brcm/BCM43341B0.hcd /lib/firmware/brcm/BCM.hcd

install package: "bluez-test" (for btmgmt) 

opensuse :

sudo zypper in bluez-test


than set to not default bt adapter mac address 

sudo btmgmt -i hci0 public-addr 43:34:1b:00:1a:ac ///for example

bluetooth should be in tray now (tested on blueman-applet)



https://lkml.iu.edu/hypermail/linux/kernel/1904.1/01727.html

also install intel-hybrid-driver for vp 8 / 9  vaapi codecs

localhost:~> vainfo
libva info: VA-API version 1.15.0
libva info: Trying to open /usr/lib64/dri/i965_drv_video.so
libva info: Found init function __vaDriverInit_1_14
libva info: va_openDriver() returns 0
vainfo: VA-API version: 1.15 (libva 2.15.0)
vainfo: Driver version: Intel i965 driver for Intel(R) CherryView - 2.4.1
vainfo: Supported profile and entrypoints
      VAProfileMPEG2Simple            :	VAEntrypointVLD
      VAProfileMPEG2Simple            :	VAEntrypointEncSlice
      VAProfileMPEG2Main              :	VAEntrypointVLD
      VAProfileMPEG2Main              :	VAEntrypointEncSlice
      VAProfileH264ConstrainedBaseline:	VAEntrypointVLD
      VAProfileH264ConstrainedBaseline:	VAEntrypointEncSlice
      VAProfileH264Main               :	VAEntrypointVLD
      VAProfileH264Main               :	VAEntrypointEncSlice
      VAProfileH264High               :	VAEntrypointVLD
      VAProfileH264High               :	VAEntrypointEncSlice
      VAProfileH264MultiviewHigh      :	VAEntrypointVLD
      VAProfileH264MultiviewHigh      :	VAEntrypointEncSlice
      VAProfileH264StereoHigh         :	VAEntrypointVLD
      VAProfileH264StereoHigh         :	VAEntrypointEncSlice
      VAProfileVC1Simple              :	VAEntrypointVLD
      VAProfileVC1Main                :	VAEntrypointVLD
      VAProfileVC1Advanced            :	VAEntrypointVLD
      VAProfileNone                   :	VAEntrypointVideoProc
      VAProfileJPEGBaseline           :	VAEntrypointVLD
      VAProfileJPEGBaseline           :	VAEntrypointEncPicture
      VAProfileVP8Version0_3          :	VAEntrypointVLD
      VAProfileVP8Version0_3          :	VAEntrypointEncSlice
      VAProfileHEVCMain               :	VAEntrypointVLD
      VAProfileVP9Profile0            :	VAEntrypointVLD
