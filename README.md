# SkywellADBOperations
Instructions how you can manage ADB operations in your Skywell ET5</br>
NOTE: For Turkish Instructions (Türkçe Yönergeler İçin): [Skywell ADB İşlemleri](https://github.com/strmotors/SkywellADBOperations/blob/main/README_TR.md)

```
███████╗████████╗   ██████╗ 
██╔════╝╚══██╔══╝   ██╔══██╗
███████╗   ██║█████╗██████╔╝
╚════██║   ██║╚════╝██╔══██╗
███████║   ██║      ██║  ██║
╚══════╝   ╚═╝      ╚═╝  ╚═╝
```

## How Can We Install Android Apps With ADB On Our Skywell ET5 Vehicle?

Herkese Merhaba,

We can use ADB (Android Debug Bridge) to delete and install applications on our Skywell ET5 vehicle. The multimedia system of our vehicle is based on the Android operating system. Every Android device has an ADB interface installed for debugging purposes. In this technique, we can connect to our agent using the ADB system, install new applications and delete these applications.

### What you need:
+ Any device that can open a personal hotspot. (Ex: Your mobile phone)
+ One computer (Windows)

### Downloads:
+ [Skywell Folder](https://drive.google.com/file/d/1_5Ux8xSb4I_E_NUmiDYTvRxZo4r_Vkwi/view?usp=sharing)

**Important Note:** If you do these steps step by step, your device will not be damaged and your device will not be out of warranty. All transactions made are reversible. In order to avoid problems on the warranty side, I suggest you delete the applications you have installed before taking the vehicle to the authorized service. In case of any problems, you can reach me at **onureser12@gmail.com** e-mail address.

#### Step 1: Installation of necessary files:

Before starting the process, you can download all the necessary files by entering this page with your computer by clicking [here](https://drive.google.com/file/d/1_5Ux8xSb4I_E_NUmiDYTvRxZo4r_Vkwi/view?usp=sharing). After extracting the "Skywell" folder from the rar file, move it to the desktop. You need to put the .apk files you want to install into this "Skywell" folder.

#### Step 2: Connecting the computer to the same Wi-Fi network as the car:

Create a personal hotspot from your phone and connect both your car and your computer to the same Wi-Fi network. Then tap the "Bluetooth Calling" section in the tool settings repeatedly until the "wifi adb opened" warning appears. At this point you will need to find out the IP address of your Car. For this, enter the Wi-Fi settings in the car settings and click on the Wi-Fi connection you are connected to. In the window that opens, you will see an IP address like "192.168.1.34".

#### Step 3: Connecting the computer to the car with ADB:

Open the "Run" window by simultaneously pressing the "Windows Key + R" keys of your computer's keyboard. In the window that opens, type ```cmd``` in the text box that says "Open:" and press the "OK" button. On the black screen that opens, ```C:\Users\Your Username>``` will be written. We can make the commands work by pressing the "Enter" key after each command we write here. We should pay attention to upper and lower case letters when writing our commands.

First of all, let's write the following command to enter the folder we put on the desktop:

```cd Desktop\Skywell```

You will now see ```C:\Users\YourUsername\Desktop\Skywell>``` on the black screen. Then, to connect to the car, let's write the following command using the IP address we learned from the car: (I went from the example of 192.168.1.34. Write whatever IP address you saw.)

```adb connect 192.168.1.34```

After the connection is established, we can install the apk file we want by typing the following command: (The info.apk file in the example is placed as an example in the Skywell folder you will download. You can install this application for trial purposes. Thanks to the info.apk application, we can see the features of the vehicle and the installed hardware.)

```adb install ./info.apk```

#### Step 4: Verify the installation:

Sometimes the download may take longer than necessary, hang or disconnect. These situations do not cause any bad consequences, you just have to repeat the process. After the installation process is finished, let's enter the application center from our vehicle. If we cannot see the application we have installed, let's close the application center and open it again by clicking the cross in the upper left.

## How Can We Delete Apps We Installed Using ADB?

Just like in the installation process, the "Skywell" folder must be on the desktop, and the car and the computer must be connected to the same Wi-Fi network in the deletion process. If these conditions are met, we can open the cmd screen again.

#### Step 1: Connecting the computer to the car with ADB:

Open the "Run" window by simultaneously pressing the "Windows Key + R" keys of your computer's keyboard. In the window that opens, type ```cmd``` in the text box that says "Open:" and press the "OK" button. On the black screen that opens, ```C:\Users\Your Username>``` will be written. We can make the commands work by pressing the "Enter" key after each command we write here. We should pay attention to upper and lower case letters when writing our commands.

First of all, let's write the following command to enter the folder we put on the desktop:

```cd Desktop\Skywell```

Let's disconnect from all devices that ADB connects to, to avoid any pre-existing connections:

```adb disconnect```

Let's connect to the vehicle using the vehicle's IP address:

```adb connect 192.168.1.34```

#### Step 2: Opening the tablet's "Settings" hidden menu using ADB:

After the ADB connection is established, we can open the "Settings" hidden menu by entering the following command. Everything you do in this menu is at your own risk.

```adb shell am start -a android.settings.SETTINGS```

You can delete the application you want by going to the application settings from the settings menu that opens.

Onur Eser

*ST-R Motors*
