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

```
<touchégg>
  <settings>
    <property name="composed_gestures_time">111</property>
  </settings>
  <application name="All">
    <gesture type="DRAG" fingers="1" direction="ALL">
      <action type="DRAG_AND_DROP">BUTTON=1</action>
    </gesture>
    <gesture type="DRAG" fingers="4" direction="DOWN">
      <action type="SEND_KEYS">Super+a</action>
    </gesture>
    <gesture type="DRAG" fingers="4" direction="UP">
      <action type="SEND_KEYS">Super+s</action>
    </gesture>
    <gesture type="DRAG" fingers="4" direction="RIGHT">
      <action type="SEND_KEYS">Super+Left</action>
    </gesture>
    <gesture type="DRAG" fingers="4" direction="LEFT">
      <action type="SEND_KEYS">Super+Right</action>
    </gesture>
    <gesture type="DRAG" fingers="3" direction="UP">
      <action type="MAXIMIZE_RESTORE_WINDOW"></action>
    </gesture>
    <gesture type="DRAG" fingers="3" direction="DOWN">
      <action type="MINIMIZE_WINDOW"></action>
    </gesture>
    <gesture type="DRAG" fingers="3" direction="RIGHT">
      <action type="SEND_KEYS">Control+Super+Right</action>
    </gesture>
    <gesture type="DRAG" fingers="3" direction="LEFT">
      <action type="SEND_KEYS">Control+Super+Left</action>
    </gesture>
    <gesture type="DRAG" fingers="2" direction="ALL">
      <action type="SCROLL">SPEED=7:INVERTED=true</action>
    </gesture>
    <gesture type="PINCH" fingers="2" direction="IN">
      <action type="SEND_KEYS">Control+minus</action>
    </gesture>
    <gesture type="PINCH" fingers="2" direction="OUT">
      <action type="SEND_KEYS">Control+plus</action>
    </gesture>
    <gesture type="TAP" fingers="3" direction="">
      <action type="MOUSE_CLICK">BUTTON=2</action>
    </gesture>
    <gesture type="TAP" fingers="2" direction="">
      <action type="MOUSE_CLICK">BUTTON=3</action>
    </gesture>
    <gesture type="TAP" fingers="1" direction="">
      <action type="MOUSE_CLICK">BUTTON=1</action>
    </gesture>
  </application>
  <application name="Gwenview, Shotwell, Evince">
    <gesture type="ROTATE" fingers="2" direction="LEFT">
      <action type="SEND_KEYS">Control+L</action>
    </gesture>
    <gesture type="PINCH" fingers="2" direction="IN">
      <action type="SEND_KEYS">Control+KP_Add</action>
    </gesture>
    <gesture type="PINCH" fingers="2" direction="OUT">
      <action type="SEND_KEYS">Control+KP_Subtract</action>
    </gesture>
    <gesture type="ROTATE" fingers="2" direction="RIGHT">
      <action type="SEND_KEYS">Control+R</action>
    </gesture>
  </application>
  <application name="Dolphin, Midori, Chromium-browser, Chrome, Firefox">
    <gesture type="DRAG" fingers="5" direction="RIGHT">
      <action type="SEND_KEYS">Alt+Home</action>
    </gesture>
    <gesture type="DRAG" fingers="5" direction="ALL">
      <action type="SEND_KEYS">Control+Next</action>
    </gesture>
  </application>
</touchégg>
```

We save our file by using STRG + O and then exit the editor by STRG + X.

Now Touchegg should provide a Mac-ish feeling. 

