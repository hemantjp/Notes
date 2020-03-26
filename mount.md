to mount with read write permission
sudo mount -t vfat /dev/sda6 /media/FAT32 -o rw,uid=$(id -u),gid=$(id -g)


sudo mount -t vfat /dev/sda6 /media/FAT32 -o uid=1000,gid=1000,umask=022
# assuming your user's UID is 1000, GID is 1000
# umask=022 sets permission mode 755 for all files on the partition

Works best 
Usually drive is mounted in /mnt/. Create a new directory in /mnt/ first.
sudo mkdir /mnt/sdb
2. Then we can mount it by:
sudo mount /dev/sdb /mnt/sdb
3. But we need to mount it for every time we reboot. To mount it automatically after each reboot, I use nano to modify the file /etc/fstab:
nano /etc/fstab
4. Enter following at the end of file:
/dev/sdb     /mnt/sdb      ext4        defaults      0       0
The first item is the path for the hard drive. The second one is the destination for the mounted drive, where we want to mount. The third one is the format type. The forth to sixth one I just kept as defaults, 0 and 0.
