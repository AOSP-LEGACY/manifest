# AOSP FOR LEGACY DEVICES

Create the source directory
---------------------------

    mkdir ~/aosp
    cd ~/aosp
    
To initialize your local repository use
---------------------------------------

    repo init -u https://github.com/AOSP-LEGACY/manifest -b ten
    
Then to sync up ( use this command for faster syncs ):
----------------

    repo sync  --force-sync --current-branch --no-tags --no-clone-bundle --optimized-fetch --prune -j$(nproc --all) -q'

Build instructions:
----------------
    . build/envsetup.sh
    lunch aosp_$device-userdebug
    mka otapackage
