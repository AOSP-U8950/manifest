aosp_manifest
================

Local Manifest to AOSP 5.1.1 for the Huawei U8950 (Honor Pro)

Build Instructions
-----------------------------------------------------------------------------

1. Initialize repo using the AOSP manifest
    
        repo init -u git://github.com/AOSP-U8950/manifest.git -b aosp-5.1


2. Then sync up the repositories
 
        repo sync


5. Build the ROM

        . build/envsetup.sh
        lunch aosp_u8950-userdebug
        make -j$(cat /proc/cpuinfo | grep -e "^processor" | wc -l) otapackage
