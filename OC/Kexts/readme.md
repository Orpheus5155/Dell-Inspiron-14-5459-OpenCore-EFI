# Kexts
Most of the kexts in this folder can be found in [Dortania's Gathering Files section](https://dortania.github.io/OpenCore-Install-Guide/ktext.html). However, you must recreate CPUFriendDataProvider by following [Dortania's Fixing Power Management guide](https://dortania.github.io/OpenCore-Post-Install/universal/pm.html#using-cpu-friend) to better suit your needs, since my own kext aren't really optimised (the battery drains a lot).

#### Headphone jack fix (Credits to EliteMacx86)
First you need to get [Jack fix script](https://elitemacx86.com/attachments/jack-fix-zip.698/) and hda-verb from [CodecCommander](https://bitbucket.org/RehabMan/os-x-eapd-codec-commander/downloads/).
Then copy hda-verb and Jack fix to bin folder by opening Terminal and type:
```
sudo cp -R /path/to/hda-verb /usr/local/bin
sudo cp -R /path/to/Jack\ fix /usr/local/bin
```
Execute the script and the audio will no longer be garbled.

You can also run the script automatically on boot by going to System Preferences, go to Users & Groups, select Login items, add Jack Fix to Login Items.
![alt text](https://elitemacx86.com/attachments/screen-shot-2019-03-29-at-6-55-51-am-png.1652/ "Adding jack fix to login items")
