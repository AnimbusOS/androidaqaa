#AnimbusOS

AnimbusOS is, at least for now, just an AOSP-ified version of [CyanogenMod](https://github.com/CyanogenMod/android)

##Getting Started

To get started with Android/AnimbusOS, you'll need to get
familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

To initialize your local repository using the CyanogenMod trees, use a command like this:

`repo init -u git://github.com/AnimbusOS/android.git -b android-6.0.1`

Then to sync up:

`repo sync`

##Building

Building works just like in cyanogenmod. `<DEVICE>` will stand for the codename of your device (For example, the Moto X 2014 is victara, and Nexus 5 is hammerhead). `<MANUFACTURER>` will stand for your device's manufacturer (For example, for the Moto X 2014 it would be motorola, and for the Nexus 6P it would be huawei)

###Getting Vendor Blobs

First off, cd into the root of your working directory and type in these commands:

`source build/envsetup.sh/`

`breakfast <DEVICE>`

Now you can go two directions here. If you have CyanogenMod running already on your device, go with the first option

*Option 1:*
Plug in your device then go to your working directory and type this command

`source vendor/<MANUFACTURER>/extract-files.sh`

*Option 2:*
Navigate to your working directory and type in:

`cd vendor && git clone https://github.com/TheMuppets/proprietary_vendor_<MANUFACTURER>.git`

then

`mv proprietary_vendor_<MANUFACTURER> <MANUFACTURER>`

###Building

Type in these commands:

`croot`

`brunch <DEVICE>`

The build will start

##Credits
* Based on CyanogenMod
* Some sources from [cm-lite](https://github.com/cm-lite)
