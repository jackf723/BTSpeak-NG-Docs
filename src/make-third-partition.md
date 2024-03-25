## Make Third Partition Help

The main thing that the make-third-partition command does is create /Public -
a directory that can be remotely accessed from a desktop, laptop, phone, tablet, etc
in order to send files to and/or get files from the BTSpeak.
The information below may be helpful to you or to your computer IT person when setting up /Public for use.

The make-third-partition command creates a third partition on the eMMC (internal disk).
This physical partition is formatted such that it contains a set of logical volumes.
It can be maintained on a running system, therefore, with Linux's lvm (logical volume management) commands.
These are usually within the /usr/sbin/ directory, and their names typically begin with
lv (logical volume), pv (physical volume), and vg (volume group).

The easiest way to run this command is to go to the Advanced System Administration menu and click on Make Third Partition.
The command itself needs to be executed as root.
It performs several steps in order to do its job.
If any of these steps has already been done then it doesn't redo it.
It's safe, therefore, to run this command more than just once.
The steps it performs are:
  1. Create a third partition on the eMMC.
  1. Format the partition as an lvm physical volume.
  1. Create a volume group named "VG_BTSpeak".
  1. Add the partition to the volume group.
  1. Create a logical volume named "Public" within the volume group.
  1. Format the public volume as an ext4 file system labelled "Public".
  1. Create a mountpoint directory for the public volume at "/Public/".
  1. Add a line to "/etc/fstab" in order to mount the public volume.
  1. Mount the public volume.
  1. Set the ownership and permissions of the public volume.
  1. Add a line to "/etc/exports" in order to export the public volume via NFS.

If the size of the eMMC is less than 20GB then the partition starts at 12GB.
If its size is 20GB or more then the partition starts at 16GB.
In both cases, it extends to the end of the eMMC.
Room is left before it so that, if needed, the size of the root file system can be increased.

The initial size of the public volume is 4 gigabytes.
Its owning user is set to "nobody", and its owning group is set to "nobody".
Its permissions are set to read, write, and search for users, group, and others (chmod ugo+rwx).
Only the user who has created a file or subdirectory within it can remove it (chmod o+t).
The owning group of the public volume is assigned to every file and subdirectory created within it (chmod g+s).

