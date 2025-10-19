# Joanslinuz
Linux distro for 486 machines

Based almost entirely on [marmolak](https://github.com/marmolak)'s awesome [gray486linux](https://github.com/marmolak/gray486linux).
I only modified the kernel config to fit it to a one floppy.

## Features
* Boots off of a 1,44 MB floppy
* Now needs ~~three~~ four floppies. One for the grub bootloader, one for the kernel, one for initramfs and one for the kernel modules
* Ships with the newest stable kernel version
* Is compatible with 486DX processors and later
* Has a bunch of modules for networking and sound support on the fourth floppy

### Building

WIP!

### Usage

1. Download the provided floppy image files 
2. * Use dd eg. `dd if=boot_grub.img of=/dev/fd0 bs=64k` to write the images to four floppies if on Linux or other unix-compatibles
   * Use rawrite if on Windows (or dd in cygwin/WSL)
3. Boot using the boot floppy, switch to kernel floppy after selecting boot option from grub and finally switch to a root floppy when prompted

### TODO

- [ ] Try to compile a static program for testing the build environment eg. nano
- [ ] Add more age-appropriate modules and hopefully fit them on one floppy.
- [ ] Fix a wrong floppy mounted error, when a correct floppy is installed (always works on the second time though...)
- [ ] Fix a annoying crng init done dmesg notification
