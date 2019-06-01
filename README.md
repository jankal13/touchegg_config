# touchegg_config
Configuration file for Touchegg to have Mac-like feeling

## Getting Started

After Touchegg is installed and we added Multigestures (e.g. through geis-tools) we need to add corresponding gestures to it. If you didn't add Multigestures yet, feel free to follow this tutorial: https://www.maketecheasier.com/add-multitouch-gestures-ubuntu/

## Commands we want

To get a Mac-like feeling for Linux we need to first know which gestures are supported by the tool. You can find the list of them here: https://github.com/JoseExposito/touchegg/wiki/All-gestures-supported-by-Touch%C3%A9gg

The actions can be found here: https://github.com/JoseExposito/touchegg/wiki/All-actions-supported-by-Touch%C3%A9gg


The actions we want to have with Touchegg are:
```
3 Fingers - Left	Go Next on Browser
3 Fingers - Right	Go Back on Browser
3 Fingers - Up	Show all Windows
3 Fingers - Down	Close Exposé (Esc)
4 Fingers - Left	Next Desktop
4 Fingers - Right	Previous Desktop
4 Fingers - Up	Next Desktop
4 Fingers - Down	Previous Desktop
```

## Steps

First we need to create the configuration file. For that we first generate the corresponding folder for Touchegg.
```
sudo mkdir ~/.config/touchegg/
```
Next, we create the config file.
```
sudo nano ~/.config/touchegg/touchegg.conf
```
After that we can add our commands to the config:
```
sudo nano ~/.config/touchegg/touchegg.conf
```
###
The commands

We start to edit the touchegg config file just like the file touchegg.conf in this rep. You can just copy & paste my template, save the file by using STRG + O and then exit the editor by STRG + X.

### Additional

You might also want to edit the ~/.xprofile file to start Touchegg on session startup. It is also provided as template in this rep.

```
sudo nano ~/.xprofile
```

Now Touchegg should provide a Mac-ish feeling. 

### Notes
I used an Asus UA330 w/ ElementaryOS Luna.

I first had problems to use Touchegg. It said something about "Failed to load canberra-gtk-module". To fix this issue you just need to provide the module:

```
sudo apt-get install libcanberra-gtk-module
```

This should fix it.

