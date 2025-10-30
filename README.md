# FOG to Snipe-IT init image files
Add an entry to [FOG](https://fogproject.org/)'s iPXE menu which allows you to upload the device's information to [Snipe-IT](https://snipeitapp.com/)

This repository contains the files changed to create this new menu entry, with each file starting as its counterpart in the original FOG init image so that it can be diff'd.

## Installation
1. First create the new menu entry in the [FOG settings](https://docs.fogproject.org/en/latest/kb/customization/advanced-boot-menu/)
2. Make a copy of your FOG init image: `cp /var/www/fog/service/ipxe/init.xz ~/init.xz.bak`. (NOTE: Yours may be in a different directory)
3. Follow the [FOG wiki](https://wiki.fogproject.org/wiki/index.php/Modifying_the_Init_Image#Modifying_the_Boot_Image) to mount your init image, keeping in mind the differing path for where FOG stores it
4. Replace all the folders which have counterparts in this repository with said counterpart. E.g.: `rm -rf initmountdir/bin && mv fog-to-snipe-it/bin initmountdir/`
5. Follow the [FOG wiki](https://wiki.fogproject.org/wiki/index.php/Modifying_the_Init_Image#Modifying_the_Boot_Image) to save your changes to the image, keeping in mind the differing path for where FOG stores it
