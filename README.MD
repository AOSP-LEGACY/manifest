<p align="center">
  <img src="https://storage.googleapis.com/gweb-uniblog-publish-prod/images/In-lineImage_1500x850.max-1000x1000.jpg" />
</p>

# AOSP 10.0 FOR LEGACY DEVICES

### Getting started:
To get started, you'll need to get familiar with [Repo](https://source.android.com/source/using-repo.html) and Version Control with [Git](https://source.android.com/source/version-control.html).

To initialize the sources locally, use a command like this:
```
$ repo init -u https://github.com/AOSP-LEGACY/manifest -b ten
```

Then to sync up:
```
$ repo sync -c -f --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

### Finally, to build: ###
```
$ source build/envsetup.sh
$ lunch aosp_<device>-userdebug
$ m -j$(nproc --all) otapackage
```
