# Joanslinuz
Linux distro for 486 machines

Based almost entirely on [marmolak](https://github.com/marmolak)'s awesome [gray486linux](https://github.com/marmolak/gray486linux).
I only modified the kernel config to fit it to a one floppy.

## Features
* Boots off of a 1,44 MB floppy
* Uses legacy grub version 0.97 to chainload initramfs from the second floppy
* Ships with the newest kernel version
* Is compatible with 486DX processors and later

### Building

WIP!

### Usage

1. Download the provided floppy image files 
2. Use dd `dd if=boot_grub.img of=/dev/fd0 bs=64k` to write the image to floppy if on Linux or other unix-compatibles
3. Use rawrite if on Windows (or cygwin/WSL)
4. Boot using the boot floppy and switch to a root floppy when prompted

### TODO

- [ ] Add more supported drivers (ATA, SCSI, sound)
- [ ] Implement module loading
- [ ] Load modules from the second floppy (create third floppy for modules???)
- [ ] Disable unneeded debug options from the kernel to save some critical floppy space



