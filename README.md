# android_twrp_device_sony_pdx206

stock twrp for sony xperia 5 ii ONLY

## Features

Works:

- ADB
- Decryption of /data (FBEv1 ONLY)
- Screen brightness settings
- Correct screenshot color
- MTP
- Flashing (opengapps, roms, images and so on)
- Backup/Restore
- Android Support from 10 up to current version
- Vibration support

## To-do
- USB OTG

## Compile

First checkout minimal twrp with omnirom tree:

```
repo init -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp -b twrp-12.1
repo sync
```

Then add these projects to .repo/manifest.xml:

```xml
<project path="device/sony/pdx206" name="lolipuru/android_twrp_device_sony_pdx206" remote="github" revision="android-12.1" />
```

Finally execute these:

```
. build/envsetup.sh
lunch twrp_pdx206-eng
mka recoveryimage
```

To test it:

```
fastboot flash out/target/product/pdx206/recovery.img
```

## Other Sources


## Thanks
- [sekaiacg](https://github.com/sekaiacg/device_xiaomi_alioth-TWRP/) for twrp base
- [ShirokaneShizuku](https://github.com/ShirokaneShizuku) for initial bringup
- [hellobbn](https://github.com/hellobbn/) for kernel source
