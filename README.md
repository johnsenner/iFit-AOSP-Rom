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

Links:

VirtualBox: https://www.virtualbox.org/wiki/Downloads
Ubuntu: https://ubuntu.com/download/desktop
repo: https://source.android.com/docs/setup/reference/repo