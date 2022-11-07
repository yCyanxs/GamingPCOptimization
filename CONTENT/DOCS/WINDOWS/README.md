## Prepare and install Windows
1. Go to https://www.microsoft.com/en-us/software-download/windows10 and Download the Windows ISO
2. Have a USB drive ready with more than 8GB of space that can be formatted and fully erased
3. Download RUFUS to manage the USB & ISO
4. Watch https://youtu.be/0s23L1m7u5I on how to use RUFUS
5. Back up your files and folders, browser bookmarks, videos, audio files or any files you may value to another separate USB drive or cloud drives before proceeding as **the next steps will erase entire hard drives**
6. Disconnect your Ethernet cable or WI-FI USB from the back of your computer for the first install
7. Restart your computer and boot from the USB drive you created using RUFUS
   - You might need to change the Boot Order in the BIOS or enter the Boot Selection menu after restarting (Each BIOS is different)
8. After booting into the Installation process, Choose your Language settings then press Install Now.
9. **Enter your Activation Key** if you have one, otherwise choose **I don't have a product key**
10. On the screen where it asks **What type of installation do you want?**, Choose **Custom: Install Windows only (advanced)**
11. Assuming you have a single disk (HDD/SSD) in the computer and no other disk in the system, for each disk present on the screen choose Delete until all the space is unallocated.
12. Press Next and Windows may indicate it will create other required partitions automatically
13. Continue through the rest of the guided setup process, note many features will be disabled after the installation if the Powershell Desired State Configuration (DSC) is used, so it won't matter what features you opt to use or not use.
