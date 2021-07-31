# Linux new machine hardware information
> uname -a

## Machine Hardware Architecture
> uname --m

## Hardware Information with lshw
> sudo lshw

## Short Summary
> lshw -short


## CPU Information with lscpu
> lscpu

![lscpu](./screenshots/lscpu.png)

## Block Device Information with lsblk
> lsblk

![lsblk](./screenshots/lsblk.png)

## USB Device Information with lsusb
> lsusb

![lsusb](./screenshots/lsusb.png)

## Disk information Human readable
> df -h

![df-h](./screenshots/df-h.png)

## Check Network card information
> lspci | grep -i 'eth'

## Short summary
> lshw -short

![short_summary](./screenshots/short_summary.png)

## Find out the IP address 
> ip addr

## Command to get complete Linux OS Info
> cat /etc/os-release

![os_info](./screenshots/os_info.png)
