Team EpicCM Device Repo
=======================

How to build
------------

* To set up the vendor tree, you'll need to `cd` to `device/samsung/epicmtd` and:

  1. Run `extract-files.sh` while phone is connected via usb to pull proprietaries from device. The script will then call `setup-makefiles` to generate `vendor/samsung/epicmtd/` and the necessary makefiles for blob manipulation.
Set java vm size
Apply platches if any
  2. Next, from the root android directory, you'll need to:

```
. build/envsetup.sh
repo sync
make clobber???
brunch epicmtd
```

and the build will begin!

At the end of the compile, the generate ota package will be in `out/target/product/epicmtd/`

so far i havent gotten the zip file to work.
but the files for this commands i have
```
$ fastboot flash boot boot.img
$ fastboot flash system system.img
$ fastboot flash recovery recovery.img
$ fastboot flash userdata userdata.img
```
