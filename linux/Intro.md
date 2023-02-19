# Intro

Basic informations
```bash
lsusb                             # shows you usb drives
sudo fdisk -l                     # shows disks
sudo parted /dev/sda 'print'      # shows partition info on /dev/sda (change /dev/sda with drive faound in previous command)
sudo blockdev --getpbsz /dev/sda  # gets you block size
```

```bash
sudo badblocks -v -n -c 256 -b 512 -s /dev/sda > badsectors.txt # generates badblocklist, change 512 to your block size (from blockdev --getpbsz)
#NTFS
sudo ntfsfix -n /dev/sda1         # check and fix (whitout -n) ntfs part
```
