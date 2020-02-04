to mount with read write permission
sudo mount -t vfat /dev/sda6 /media/FAT32 -o rw,uid=$(id -u),gid=$(id -g)


sudo mount -t vfat /dev/sda6 /media/FAT32 -o uid=1000,gid=1000,umask=022
# assuming your user's UID is 1000, GID is 1000
# umask=022 sets permission mode 755 for all files on the partition
