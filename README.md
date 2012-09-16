# flash-utils

This repository tracks the code from the TI DVSDK psp/flash-utils directory
which contains (among other things) the source code to the UBL bootloader.

## Building instructions

Make sure that the CodeSourcery ARM compiler is in the path.

cd DM36x/GNU/ubl
make

The file ubl_DM36x_dm365sdmmc.bin will be created. Supposing everything works,
this should be a good UBL bootloader that can be written to an SDCard and
booted from. See the u-boot project for writing the UBL and U-boot to an
SDCard.

## Updating

If TI updates their DVSDK, it may be nice to update the UBL if they fixed
something good or moved some initialization from u-boot or later to the UBL. It
is probably easiest to branch off the initial comment, apply TI's updates, and
then merge back to master. 

