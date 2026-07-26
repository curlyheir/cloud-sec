## fixed fake usb from bash


tried to format it kept getting error [ error mounting filesystem udisks-error-quark 14 ]

# install f3

sudo apt update
sudo apt install f3


# find device identifier name

'''bash
lsblk
'''
- look at the bottom in sdb and you will find it

# find device true size 

Use [f3probe] to determine device true capacity.

sudo f3probe --destructive --time-ops /dev/sdb

# fix partition

sudo f3fix --last-sec=12345678 /dev/sdb

- change that number to the actual size number of the partition table

# finalize 

sudo mkfs.vfat /dev/sdX1 

- the 1 at the end indicating a new partion

1. Find the Correct Device Name Run lsblk to identify your USB drive. Look for the device matching your USB's size.

'''bash
lsblk
'''

2. Unmount the Drive You cannot format a mounted drive. Unmount it using the mount point or the device name:

sudo umount "/path/to/drive"
# OR
sudo umount /dev/sdb1

3. Format Using the  [Device Identifier] Run the format command on the /dev/sdX# path, not the /run/media/... path:

sudo mkfs.ext4 /dev/sdb1 -L "USB_LABEL"

# error conclusion 1 

Argument Parsing: Because your folder name contains spaces and numbers (UBUNTU 26_0), the shell or mkfs likely parsed 26_0 as a separate argument. mkfs.ext4 accepts an optional [blocks-count] argument after the device; it tried to create a filesystem of exactly "26_0" blocks (or failed to parse it), causing the size mismatch error.

# error conclusion 2

Wrong Target: /run/media/... is a directory where the file system is accessed, not the raw device.

# if target is busy as you are trying to format

1. sudo umount "/run/media/path" 

2. sudo lsof +f -- "/run/media/path/to/device"
# OR
sudo fuser -vm "/run/media/path/to/device"

3. Terminate the listed processes (using kill <PID>) or close the application, then retry umount 

sudo kill -9 <PID> or sudo fuser -km "/run/media/path/to/device"

flag -k kills processes flag -m specifies mount point.

4. 4. Retry Formatting Once unmounted successfully, run the format command on the device identifier (e.g., /dev/sdb1), not the mount path:

#unmount if auto-mounted
sudo umount /dev/sdb1

# format as FAT32 (recommended forcapability or ext4
sudo mkfs.fat -F 32 /dev/sdb1 -n "FIXED_USB"


- at this point, i fixed the partition tables from 1.9 tb to 59.2 gb & formated it to EXFAT32.

