near AOSP ROM (nAOSP) for Sony Xperia S (nozomi)

This branch is derived from bAOSP and include some improvements.

New features:

    Device : AOSP code fix to support full features of this device (eg: FMradio)
    Busybox
    Recovery : FOTAkernel only. You can flash TWRP/CWM into mmcblk0p11
    Email : Fake security for Exchange (remove pin, remote erase ...)
    Su    : Integration of Superuser into Settings and support of su
    Power menu : Enhanced power menu with reboot support
    Quick setting : pull down with one finger on the right side of status bar
    Recent apps : add clear all recent applications

1. initialize the repo:

    repo init -u https://github.com/mickybart/android_manifest -b nAOSP-5.0

2. sync repo:

    repo sync

3. build:

    - source build/envsetup.sh
    - lunch aosp_nozomi-userdebug
    - export USE_CCACHE=1
    - export CCACHE_DIR=.ccache
    - prebuilts/misc/linux-x86/ccache/ccache -M 50G
    - make

    (see: http://source.android.com/source/building.html)
