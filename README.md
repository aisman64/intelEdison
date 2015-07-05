#Tutorial for programming the Grove Starter Kit on Yocto

##Before Starting
###    This tutorial has been designed for and tested on Windows 8.1 x64, Mac steps should be similar, but not identical
###    Downloads
        All-in-One Installer: http://downloadmirror.intel.com/25028/eng/iotdk_win_installer.exe
        PuTTY: http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html
        Intel IoT XDK Installer: https://software.intel.com/en-us/html5/xdk-iot

##Setting up your Edison
    If using the Arduino Kit, you will need a 7~15V power brick, usb will probably not have enough power
    If you are using the small breakboard kit, it should be fine using two USBs
    Connect the Grove Kit's Arduino Shield
    Connect the Touch Sensor to port D2
    Connect the Buzzer to port D6 
    Plug your Edison into the computer (Both USB Ports)
    Run the All-in-One installer
    Search for the COM port, it should say "USB Serial Port"
    Connect to this port using PuTTY, baud rate 115200 
    Login is "root", password is empty
    Now run the command "configure_edison --setup" and set up your Edison 
    Connect to a wireless network using "configure_edison --wifi"
    Execute these commands to enable your WiFi connection
        ifconfig usb0 down
        ifconfig wlan0 down
        ifconfig wlan0 up
    Write down your IP Address
        You can get it by running "ifconfig wlan0"

##Installing MRAA (Run the following commands):
    echo "src maa-upm http://iotdk.intel.com/repos/1.1/intelgalactic" > /etc/opkg/intel-iotdk.conf
    opkg update
    opkg upgrade
    reboot

##Installing IoT XDK:
    Run the Installer
    Open the IoT XDK
    Create an Intel Account
    Login with your Intel Account

##Start Programming (Edison)
    Start a New Project > Internet of Things Embedded Application > Templates > Touch Notifier
    Continue
    Write a name for your project
    Select your IoT Device
    Connect to your IoT Device
    Press Install/Build (2nd button to the right of Select your IoT Device)
        On the PopUp, press build
    Press Upload (1st button to the right of Select your IoT Device)

##Start Programming (Companion App)
    Start a New Project > HTML5 Companion Hybrid Mobile or Web App > Samples and Demos > General > HTML5 + Cordova > Touch Notifier
    Continue
    Write a name for your project
    Press Run My App (Right Hand)
        Run in Emulator
    Write the IP Address of your Edison on the first box
    On the 2nd box, write "1337" (No quotes)
    

##Test
    Press the touch button, the buzzer should buzz and you should get a notification in your cellphone, otherwise retrace the steps above
 
##Resources
    Sparkfun Edison Getting Started Guide: https://learn.sparkfun.com/tutorials/edison-getting-started-guide


##FAQ
###I can't connect to my Edison's serial port, what is wrong?
   Check if the Edison has been secured properly with the nuts
   Check that the serial port is the correct one
