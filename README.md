Files required for building a guest kernel image
==========

These files are required when building the image for a basic guest kernel.

Prerequisites:
----------
FreeBSD-UPB/freebsd
FreeBSD-UPB/bhyvearm-utils

The files here should be moved to their respective subdirectories in the
'freebsd' project. After running the 'build_ramdisk.sh' script once (after building
the freebsd world), you may build the kernel for the guest.

Basic run command order:
------------
The following commands assume that the repositories were downloaded in /root/
directly. If the path is different, please correct the path specified in the
'FVP_VE_CORTEX_A15x1_GUEST' file.

/root/freebsd/$ make buildworld  
/root/bhyve-utils/ramdisk/$ bash build_ramdisk.sh  
/root/freebsd/$ make buildkernel KERNCONF=FVP_VE_CORTEX_A15x1_GUEST
