# Aosp Manifest

**Downloading the Source**

The Android source tree is located in a Git repository hosted by Google. The Git repository includes metadata for the Android source, including changes to the source and when the changes were made. This page describes how to download the source tree for a specific Android code line.

To start with a factory image for a specific device instead of downloading the source, see Selecting a device build.

Initializing a Repo client 
After installing the Repo Launcher, set up your client to access the Android source repository:

Create an empty directory to hold your working files. Give it any name you like:


```
mkdir cy
cd cy
```
Configure Git with your real name and email address. To use the Gerrit code-review tool, you need an email address that's connected with a registered Google account. Ensure that this is a live address where you can receive messages. The name that you provide here shows up in attributions for your code submissions.


```git config --global user.name Your Name
git config --global user.email you@example.com
```

Run repo init to get the latest version of Repo with its most recent bug fixes. You must specify a URL for the manifest, which specifies where the various repositories included in the Android source are placed within your working directory.


`repo init -u https://android.googlesource.com/platform/manifest -b android-12.1.0_r2`


# Cyclone Manifest
1.Now create a local_manifests dir and Copy the required manifests in that folder.

``` 
mkdir .repo/local_manifests
wget -O .repo/local_manifests/cyclone.xml 'https://raw.githubusercontent.com/ProjectCyclone/manifest_cyclone/main/cyclone.xml
```
2.Then to sync up:

    repo sync -c -f --force-sync

OR, for those with limited bandwidth/storage:

    repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
