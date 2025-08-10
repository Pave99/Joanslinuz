# Joanslinuz
Linux distro for 486 machines

Based almost entirely on [marmolak](https://github.com/marmolak)'s awesome [gray486linux](https://github.com/marmolak/gray486linux).
I only modified the kernel config to fit it to a one floppy.

## Features
* Boots off of a 1,44 MB floppy
* ~~Uses legacy grub version 0.97 to chainload initramfs from the second floppy~~
* Now needs three floppies. One for the grub bootloader, one for the kernel and one for initramfs
* Ships with the newest kernel version
* Is compatible with 486DX processors and later

### Building

WIP!

### Usage

1. Download the provided floppy image files 
2. Use dd eg. `dd if=boot_grub.img of=/dev/fd0 bs=64k` to write the images to three floppies if on Linux or other unix-compatibles
3. Use rawrite if on Windows (or dd in cygwin/WSL)
4. Boot using the boot floppy, switch to kernel floppy after selecting boot option from grub and finally switch to a root floppy when prompted

### TODO

- [X] Add more supported drivers (ATA, SCSI, sound)
- [X] Implement module loading
- [ ] Load modules from the initramfs floppy (hopefully fit all required modules with busybox to initramfs floppy...) 
- [ ] Disable unneeded debug options from the kernel to save some critical floppy space
- [ ] Test module loading with simple serial module 
