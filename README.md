# hello-world
GHOST FRAFRAMEWORK
Ghost Framework -- Control Android Devices Remotely



Ghost Framework is an Android post-exploitation framework that uses an

Android Debug Bridge to remotely access and control devices

Ghost Framework gives us the power and convenience of remote Android device administration.




Remotely control android using ghosts




We can use this framework to control old Android devices which have turn on the debug bridge in the "Developer options".



Now this becomes very harmful because an attacker gets the full admin control on the vulnerable Android device.

In our this detailed tutorial we will practically learn how we can use the Ghost Framework to take control of Android device from our Kali Linux system.



So we start from cloning the Ghost Framework from GitHub by using following command:

git clone https://github.com/entynetproject/ghost
The screenshot of the command is following:




clonning ghost from github




Then it will be cloned on our root folder of Kali Linux. Then we go the ghost directory by using cd command:

cd ghost
Now we need to install it using the installer script. Before that we give the permission to the installer script by applying following command:

sudo chmod +x install.sh
Here if it prompted for sudo password of our machine then we need to provide it.




giving root permission




Now we can run the installer script using following command:



sudo ./install.sh
Then wit will start installing the dependencies and as the following screenshot:




installing ghost in our Kali Linux


This process will take some time depending our internet speed.



After installing Ghost Framework we can run it from any where in our terminal by only the ghost command:



sudo ghost
And the ghost will appear with it's main screen as the following screenshot:


ghost




Now we can see the options by using help command.

help
The help option will be like following screenshot:


ghost help
In the above screenshot we can see that we can connect vulnerable Android device by it's IP with the help of connect command:.



Now how we get a IP address of an Old vulnerable Android devices? Shodan is here. Shodan is a grate search engine for searching the devices connected to internet. We already have a tutorial on Shodan.



In Shodan we have to search "Android Debug Bridge", as we have shown in following screenshot:




shodan android debug bridge




Here we can see over 19k search results. Every device is vulnerable for ghost and those devices are connected to internet.



From here we can pick any IP address and use with connect command.

connect 221.211.29.92
We got connected with this device as we see the screenshot below.




Here we can see we are connected with the IP address. Now we can run anything from Ghost Framework.



We can see the commands we can run after connecting by using help command again.

help

ghost framework main options


What we can do with Ghost Framework:
Show connected devices
Disconnect all devices
Connect a new device
Access device shell
Install an apk on a device
Screen record a device
Get device screenshot
Restart Ghost Server
Pull files from devices
Shutdown the device
Uninstall an app
Show device log
Dump system Info
List of all device app
Run a device app
Port Forwarding
Grab wpa_supplicant(WiFi password)
Show Mac/Inct
Extract apk from app
Get Battery Status
Get Network Status
Turn WiFi on/off
Remove device password
Emulate button presses
Get Current Activity
Update Ghost Framework
Exit Ghost Framework
For an example we connect to the Android shell of connected device.

shell

shell on compromised android device




Ghost Framework has a simple and clear UX/UI. It is easy to understand and it will be easier for us to master the Ghost Framework.



Ghost Framework can be used to remove the remote Android device password if it was forgotten. It is also can be used to access the remote Android device shell without using OpenSSH or other protocols.



[UPDATE] Many user got error like this "Failed to start Ghost Server". In that case ADB (Android Debug Bus) and fastboot need to be install manually. Try following commands if this kind of error comes:



sudo apt-get update
sudo apt-get install android-tools-adb
sudo apt-get install android-tools-fastboot
⭕⭕⭕⭕⭕⭕⭕⭕⭕⭕⭕⭕⭕⭕

Ghost uninstallation
cd ghost
chmod +x uninstall.sh
./uninstall.sh





