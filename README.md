# 32 bit EFI files

Some older computers only support the 32 bit EFI boot.
One of them is the Mac Mini 2.1. Although it can run a 64 bit OS,
it only supports 32 bit EFI boot partitions.

# Example
If you want to install Debian on a Mac Mini 2.1 with Core2Duo.
The debian-mac-12.5.0-amd64-netinst.iso was not working for me.
This workaround is tested with Debian-12.5-amd64 on a Mac Mini 2.1 with 2GB ram and Core2Duo CPU.

To make it work:
1. Download debian-xxx-amd64-netinst.iso https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/
2. On windows use Rufus to burn ISO to USB stick.
3. Copy files in boot\grub to USB installer boot\grub, keep boot\efi.img, boot\font.pf2, boot\grub.cnf
4. Copy EFI to  USB installer boot\grub
5. Now install Debian and it will work. It seems that Debian can detect that a 32bit UEFI is required.


Thanks to Frank Aalbers that have publish the orginal working UEFI files at https://github.com/faalbers/EFI_32_BIT for Ubuntu.

