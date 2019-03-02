## disk utilities

```
# list disk devices
diskutil list

# unmount disk
sudo unmount <disk name>

# copy disk image to target device
sudo dd if=<input file> of=/dev/r<disk name> bs=1m

```