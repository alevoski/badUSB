# BadUSB
![Platform](https://img.shields.io/badge/plateform-windows%20%7C%20linux-lightgrey.svg)  

This project is a study about bad-USB.  
Project in construction  

## Intro ##
BadUSB devices areUSB devices with a cpu that can execute scripts automatically  
when they are mount on a computer.  
Computers reconize them as "trust worthly devices" like HID devices (ie : Keyboards)  
They cannot be detected by antivirus.  
A badUSB device can do the same actions than a keyboard.


## How to protect ? ##
Sevaral actions can be done to prevent troubles :  
 - Autolock computer option is not sufficiant : ***if you leave your computer just lock your session***  
 - ***Don't use your administrator privileges if you don't need them***  
 - ***Never trust unrecognized USB devices (and any devices gloabaly)***  
    - You should at least scan the device for viruses (with [Decontamine_Linux](https://github.com/alevoski/decontamine_Linux))  
    - Remembered that a classic antivirus will not detect anything from an encoded binary payload  
    - Any doubts : don't insert the device on your computer !  
    - Keep in mind that some rogue USB devices can simply [physically destroy your computer](https://thehackernews.com/2016/09/usb-kill-computer.html)  
- For Windows sysadmin : a  kind of secure GPO will save your users from this
    - Block access to CMD by all means 
    - Disable Windows shortcuts
    - Block access to control panel 
    - Or at least, ***your users shouldn't have administrator rights***

## Getting Started
Download the project on your computer.
```
git clone https://github.com/alevoski/badUSB.git
```

### Prerequisites
[An Hak5 Rubber Ducky](https://shop.hak5.org/products/usb-rubber-ducky-deluxe)  
A SD card  
A SD card reader  
[Hak5 tools to create payloads](https://github.com/hak5darren/USB-Rubber-Ducky)  

### HOW TO REPRODUCE THE EXAMPLES ?
I provide the encoded payload but if you prefer you can go to the EXAMPLES/ folder and make the payload yourself  
```
java -jar encoder.jar -i <pathofyourcodetobeencoded> -o <outputpath> -l <yourlangage>
java -jar encoder.jar -i /home/userX/hello -o /home/userX/hello.bin -l en
```

#### Demos (Windows OS)  
*** Hello World ***  
![](DOCS/DEMOS/hello.gif)  

*** Control Panel ***  
![](DOCS/DEMOS/controlPanel.gif)  

*** Fake update ***  
![](DOCS/DEMOS/fakeUpdate.gif)  

*** Password dump***  
![](DOCS/DEMOS/passdump.gif)  

## Author
Alexandre Buissé



