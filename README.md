# usbboot_rpi
Instructions for cloning SD card and booting from external USB drive

## WARNINGS and DISCLAIMER
*The following tools used can potentially harm or damage the file system if used improperly.  It is recommend that you verify first using a fresh SD card image and then after successfully completing the instruction repet on the live system to mitgate any damage or loss of data to a production released system.  The author of this repository is not to be held responsible for any loss of data or damage caused to the system. Proceed only under your own free will and at your own risk!*

## Quick start 
This method utilizes GUI interfaces and CLI to prepare USB boot

### Prepare external USB drive
- Clear disk partitions
    - Insert external usb drive
    - Find your disk be careful and eject if necessary to verify
    *typically /dev/sda if only disk mounted as for example below*
    ```
    sudo ls -al /dev/sd*
    ``` 
    - Delete old and create new partitions
      - Open gparted
      - Select proper disk under menu GParted/Devices identified in prior steps
      - Remove all partitions using menu Partition/delete until entire disk is unallocated
      - Create boot partition
          - Select menu Device/Create Partition Table as MSDOS and Apply
          - Create new primary partition table for boot with a minimum size of 250MB >= 239 MiB
          - Click menu Partition/New
          - Click Add
        [IMG]
          - Write changes to disk with menu Edit/Apply All Operations and click Apply
      - Flag boot partition as bootable by right clicking on partition
          - Select Manage Flags
          - Select check both lvb and boot
            [IMG]
      - Create root partition from unallocated space
          - Click menu Partition/New
          - Update file system type to ext4
          - Click Add
          - Select menu Edit/Apply All operations to write changes to disk
          - Click Apply                
        
## Create SD for EEPROM bootloader flash

  
## Long method using CLI
This method is meant to be used in cases where only a CLI interface to the RPI is available




- Choose RPI hardware
  [IMG]   
- Select Erase and format entire external drive as FAT32
