#AnimbusOS

AnimbusOS is, at least for now, just AOSP

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

`//`

`make clobber`

`. build/envsetup.sh`

###Building

Type in these commands:

`croot`

`lunch aosp_<DEVICE>-userdebug`

`make -j#` (# being the number of logical cores on the device)

The build will start

##Credits
* Based on AOSP
* Some sources from [cm-lite](https://github.com/cm-lite)
