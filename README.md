# C740-14iml-BigSur
## EFI for Lenovo C740 on BigSur with Opencore

This EFI guide was based on Dortania use of Opencore

The versions used are Opencore 0.7.2
Big sur install on 11.5.2

C740 specs:
1. i7-10710U 4.60 ghz 12mb cache 
2. 16 gbs ram
3. intel UHD-620 graphics
4. 250 Western digital sn750  <del>intel 512 ssd with 32 optane memory module</del>
5. Intel Wi-Fi 6 22560 2x2 AX, Bluetooth version 4.3
7. ps2 keyboard
8. i2cHID trackpad
9. Wacom touchscreen 14"fhd
10. 1 usb-c, 1 thunderbolt, 1 usb-a

## What is currently working

- Accelerated graphics
- Audio codec
- Keyboard with brightness control and volume control
- intel energy prophile
- mapped usb ports, but I'm not sure if they are correct as I can't try them all
- SDST's (however I suspect they may be more customs to make the trackpad work)
- HDMI output trough usb-c (display port output) (turns out we need a smbios without egpu)

## What **isn't** working
- Trackpad
- Touchscreen
- Bluetooth is buggy
- Haven't tried i-services
- Haven't tried encription security
- intel wifi is not working to max speed, but the fact that it is working nicely is pretty impressive
- Log-in chime

## Installation
- usb2.0 with full install rom on APFS
- Mono boot
- note that the intel UHD appears with no number on model and description page, but we have 620 for plist related affairs
- make sure you use ProperTree.py to update the plist with ctrl+r before deploying to make sure the pathings are ok 
