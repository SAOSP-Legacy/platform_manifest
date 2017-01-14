##Initialize the source##
repo init -u https://github.com/SAOSP-Legacy/platform_manifest.git -b N1

##Sync the source##
repo sync -jx -f (x being however many cpu jobs)

##Setup build environment##
. build/envsetup.sh

##Get the right device to build##
lunch saosp_mako-userdebug
lunch saosp_flo-userdebug
lunch saosp_hammerhead-userdebug

##Build it##
make otapackage -jx (x being however many cpu jobs)

##Credits##
Google for AOSP, Rascarlo and Rastakat for a lot for commits, AOSPA, CM, Other that we may missed, Etc.

