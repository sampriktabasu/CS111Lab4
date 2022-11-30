# Hey! I'm Filing Here

Creating a 1MiB ext2 file system with 2 directories, 1 regular file, and 1 symbolic link.

## Building

To build the program run the following command...
```make```

## Running

Run the executable and create base image:
```
./ext2-create.c
```
Mount the filesystem:
```
mkdir mnt
sudo mount -o loop cs111-base.mnt   
```
Switch into mounted directory `cd mnt`. Example output of 'ls-ain' here...
```
total 7
      2 drwxr-xr-x 3	0	0 1024 Nov 30 11:38 .
 942226 drwxr-xr-x 5 1000    1000 4096 Nov 30 11:38 ..
     13 lrw-r--r-- 1 1000    1000   11 Nov 30 11:38 hello -> hello-world
     12 -rw-r--r-- 1 1000    1000   12 Nov 30 11:38 hello-world
     11 drwxr-rr-x 2 	0       0 1024 Nov 30 11:38 lost+found
```

## Cleaning up

Explain briefly how to unmount the filesystem, remove the mount directory, and
clean up all binary files.
Unmount the filesystem:
```lab4 $ cd mnt```
```lab4/mnt $ sudo umount mnt```

Remove the mount directory:
```lab4 $ rmdir mnt```

Clean up binary files:
```lab4 $ make clean```
