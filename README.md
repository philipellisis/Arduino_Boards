# Cleveland Software Design Arduino Board

This repository contains support for the cleveland software design board specifically made for use in virtual pinball machines, but it will work with a standard Arduino board that uses the ATmega32U board

### Installation Instructions

To add board support for our products, start Arduino and open the Preferences window (**File** > **Preferences**). Now copy and paste the following URL into the 'Additional Boards Manager URLs' input field:

	https://raw.githubusercontent.com/philipellisis/Arduino_Boards/main/IDE_Board_Manager/package_clevsoft_index.json


If there is already an URL from another manufacturer in that field, click the button at the right end of the field. This will open an editing window allowing you to paste the above URL onto a new line.

### ClevSoft Installation Instructions

Open the Boards Manager window by selecting **Tools** > **Board**, scroll to the top of the board list, and select **Boards Manager**.


If you type "clevsoft" (without quotes) into the "filter your search" field, you will see options to install clevsoft's AVR board files. Click in the desired box, and click the "Install" button that appears. Once installed, the boards will appear at the bottom of the board list.


### Notes

* Some boards such as the Arduino Pro and Pro Mini come in more than one flavor.  For these **you must select the correct processor** in the 'Tools' menu.
* Information on compiling and programming the bootloaders can be found in the bootloaders directory.

#### updating package.json file
 - unzip file: tar -xf clevsoftboards.1.1.14.tar.gz
 - make changes and zip file back: tar -czvf clevsoftboards.1.1.14.tar.gz avr
 - update package with checksum: sha256sum clevsoftboards.1.1.14.tar.gz
 - update package with size: ls -l

#### testing locally

You can test new implementations by navigating to C:\Users\{user}\AppData\Local\Arduino15\packages\ClevSoft\hardware\avr\1.1.14 and adjusting files as needed.
