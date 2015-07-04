#Tutorial for programming the Grove Starter Kit on Yocto

##Before Starting
###    We are assuming that you are using Windows for this tutorial, it has only been tested on Windows 8.1 x64
###    Downloads
        All-in-One Installer: http://downloadmirror.intel.com/25028/eng/iotdk_win_installer.exe
        PuTTY: http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html
        Intel IoT XDK Installer: https://software.intel.com/en-us/html5/xdk-iot


##Setting up your Edison
    If using the Arduino Kit, you will need a 7~15V power brick, usb will probably not have enough power
    If you are using the small breakboard kit, it should be fine using two USBs
    Plug your Edison into the computer (Both USB Ports)
    Run the All-in-One installer
    Search for the COM port, it should say "USB Serial Port"
    Connect to this port using PuTTY, baud rate 115200 
    Login is "root", password is empty
    Now run the command "configure_edison --setup" and set up your Edison 

##Installing MRAA (Run the following commands):
    echo "src maa-upm http://iotdk.intel.com/repos/1.1/intelgalactic" > /etc/opkg/intel-iotdk.conf
    opkg update
    opkg upgrade
    reboot

##Installing IoT XDK:
    Run the Installer
    Create an Intel Account
        



##Resources
    Sparkfun Edison Getting Started Guide: https://learn.sparkfun.com/tutorials/edison-getting-started-guide
