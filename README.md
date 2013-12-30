CyanogenMod 10 for the HTC Wildfire S
=============

Getting Started
---------------

To get started with Android/CyanogenMod, you'll need to get
familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

Syncing
-------
    repo init -u git://github.com/olivieer/android.git -b jellybean
    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.github.com/olivieer/cm10-manifest/master/local_manifest.xml
    repo sync
    
Building
--------
    cd ~/<WORKING FOLDER>;repo sync;./vendor/cm/get-prebuilts;cd bionic;git fetch http://review.cyanogenmod.com/CyanogenMod/android_bionic refs/changes/31/14631/1 && git cherry-pick FETCH_HEAD;cd ..;cd hardware/msm7k;git fetch http://review.cyanogenmod.com/CyanogenMod/android_hardware_msm7k refs/changes/58/15058/3 && git cherry-pick FETCH_HEAD;cd ..;cd ..;source build/envsetup.sh; lunch cm_marvel-eng
    make -jX bacon
    
Credits
-------
- modpunk (aka cryptomilk, gladiac, asn)
- CyanogenMod Team
- androidarmv6 Team
- OliverG96
