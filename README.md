# iFit-AOSP-Rom

Doc: Getting started on AOSP Development

You will need:
A _linux_ workstation or VM
A few hours to download stuff, on a good internet connection

Choose a directory, maybe "aosp/". Clone the AOSP manifest repository from Google's Git server:

git clone https://android.googlesource.com/platform/manifest aosp

Download the repo tool binary and save it to ~/.bin.

curl https://storage.googleapis.com/git-repo-downloads/repo > ~/.bin/repo

Change permissions of the repo tool binary to make it executable.

chmod a+rx ~/.bin/repo

Open the .bash_profile file in a text editor.

code ~/.bash_profile

Prepend ~/.bin to the PATH environment variable.

PATH="${HOME}/.bin:${PATH}"

Initialize the repo tool with the main branch of the AOSP manifest. (info on Google's repo tool at )

repo init -b main -u https://android.googlesource.com/platform/manifest

Synchronize the local repository with the AOSP repositories specified in the manifest.

repo sync -c -j8

Initialize repo with the Android P Preview 4 branch of the AOSP manifest.

repo init -u https://android.googlesource.com/platform/manifest -b android-p-preview-4

Initialize repo with the Android P Preview 4 branch of the AOSP manifest.

repo init -u https://android.googlesource.com/platform/manifest -b android-p-preview-4

Build AOSP:

source build/envsetup.sh
lunch <device_codename>-userdebug
make -j8

device_codename: If you're building a custom ROM for a specific device, you'll need to use the correct <device_codename> for that device. Here are a few examples of device codenames for popular Android devices:

Nexus 5X: bullhead
Nexus 6P: angler
Pixel: sailfish (Pixel 1), marlin (Pixel XL), walleye (Pixel 2), taimen (Pixel 2 XL)
Samsung Galaxy S10: beyond1lte
Samsung Galaxy Note 10: d1

Example:
lunch bullhead-userdebug


Links:

VirtualBox: https://www.virtualbox.org/wiki/Downloads
Ubuntu: https://ubuntu.com/download/desktop
repo: https://source.android.com/docs/setup/reference/repo