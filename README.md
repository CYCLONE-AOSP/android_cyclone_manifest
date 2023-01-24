Cyclone
========

Getting Started
---------------

To get started with Android, you'll need to get
familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

To initialize your local repository using the Cyclone trees, use a command like this:

```bash
repo init -u https://github.com/CYCLONE-AOSP/android_cyclone_manifest.git -b thirteen-august
```
Then to sync up:
```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

Building the source
---------------
```bash
. build/envsetup.sh
lunch aosp_<device>-userdebug
mka bacon (or) brunch <device>
```