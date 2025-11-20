# Pseudo Character Device Driver
A simple Linux kernel module implementing a pseudo character driver.
## Features
- Supports `open`, `release`, `read`, `write`, `llseek`
- Uses 512-byte buffer as device memory
- Creates `/dev/pcd` via sysfs class
## Build & Run
```bash
make
sudo insmod pcd_driver.ko
ls -l /dev/pcd
echo "Hello" > /dev/pcd
cat /dev/pcd
sudo rmmod pcd_driver
