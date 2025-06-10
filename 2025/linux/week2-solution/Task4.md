Volume Management & Disk Usage


Managing storage volumes and disks is vital for Linux admins.

Create mount point directory:

```bash
  sudo mkdir /mnt/devops_data
```

Mount a volume or loop device: For local testing, create a loop device from a file:

```bash
  sudo dd if=/dev/zero of=/tmp/devops_volume.img bs=1M count=100
  sudo losetup /dev/loop0 /tmp/devops_volume.img
  sudo mkfs.ext4 /dev/loop0
  sudo mount /dev/loop0 /mnt/devops_data
```

Verify mount:

```bash
  df -h | grep devops_data
  mount | grep devops_data
```
