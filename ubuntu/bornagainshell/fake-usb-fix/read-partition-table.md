# re-reading partition table

1. Unmount All Partitions
First, ensure no partition on the drive is mounted. Replace sdX with your device (e.g., sdb):

sudo umount /dev/sdb*

2. Force the Kernel to Re-read
Once unmounted, run one of the following commands to refresh the partition table:

Option A: Using partprobe (Recommended)

sudo partprobe /dev/sdb

# if target is still busy

1. Find the Mount Point
First, find where the drive is mounted (e.g., /media/usb):

lsblk -f /dev/sdb

2. identify PID process holding drive

sudo fuser -mv /mount/point

3. kill processes 

sudo fuser -kmv /mount/point 
or
lsof +f -- /mount/point
kill -9 <PID>

4. Retry Unmounting 

sudo partprobe /dev/sdb

5. check if new partition is visible

lsblk /dev/sdb 
