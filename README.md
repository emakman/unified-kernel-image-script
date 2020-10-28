unified-kernel-image-script
---------------------------
This is a simple bash script and pacman hook to generate unified kernel images when the kernel is updated. The target is arch-based distros, but if it works on your distro, great.

Usage
-----
After downloading, simply run `sudo ./install` to install the package. This will install an example configuration file at `/etc/uki-script/linux.conf.example`
Copy that file to `/etc/uki-script/<your kernel name>.conf` and edit it to meet your needs.

If you would like to generate images for multiple kernels (or multiple images with different kernel command lines) then make separate configuration files for each.

Run `sudo uki-script` to test your configuration and verify that the images were built (and installed). You should not need to run `uki-script` manually again since it is called by the pacman hook when the kernel is updated.
