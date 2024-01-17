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
    - Open open fdisk on selected disk
    ```
    sudo fdisk /dev/sda
    ```
    - Expect return
    Welcome to fdisk (util-linux 2.37.2).
    Changes will remain in memory only, until you decide to write them.
    Be careful before using the write command.
    
    Device does not contain a recognized partition table.
    Created a new DOS disklabel with disk identifier 0x2c5a44ea.
    
    Command (m for help): 
- Updated partition table
  - Open gparted
  - Change partition flags 
    - Right click on partition
    - Select Update flags
    - LBA should be checked in addition check boot
    [IMG]
  - Resize
    - Menu select Partition/Unmount
    - 
    
-   ## Create SD for EEPROM bootloader flash
## Long method using CLI
This method is meant to be used in cases where only a CLI interface to the RPI is available




- Choose RPI hardware
  [IMG]   
- Select Erase and format entire external drive as FAT32
