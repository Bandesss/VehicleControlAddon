# VehicleControlAddon for Farming Simulator 2019

## How to download?

Just click here: [Latest version](https://github.com/Mogli12/VehicleControlAddon/blob/master/FS19_VehicleControlAddon.zip?raw=true)

## Status
I will not publish FS19_VehicleControlAddon anymore. I continue to work on this mod only for my own purpose. Do not expect that I will fix problems you find.

Saving settings is now user dependent. I hope it does not break loading of saving games in MP. Please follow up in [#143](https://github.com/Mogli12/VehicleControlAddon/issues/143).

I re-implemented the adaptive steering. The old implementation was too simillar to the vanilla steering. If you have problems with automatic back rotation just press the key to steer into the opposite direction.

If you are looking for a realistic manual transmisison please visit [FS19_realManualTransmission](https://github.com/modelleicher/FS19_realManualTransmission)

I added several settings for players with a gear shifter. These are the different options:
* "6G, 1R, LH" - 6 gears, 1 reverse gear, one button to swtich between low and high range
* "6G, Shuttle, LH" - 6 gears, one button to change driving direction, one button to swtich between low and high range
* "6G, D/R, LH" - for 8+1 shifters: 6 gears, gear 7 switches to forward, gear 8 switches to backward, one button to swtich between low and high range
* "6G, R+/-, 1R" - for 8+1 shifters: 6 gears, gear 7 increases the range, gear 8 lowers the range, gear 9 switches into the single reverse gear
* "6G, R+/-, Shuttle" - for 8+1 shifters: 6 gears, gear 7 increases the range, gear 8 lowers the range, gear 9 toggles the driving direction
* "8G, 1R, LH" - for 8+1 shifters: 8 gears, 1 reverse gear, one button to swtich between low and high range
* "8G, Shuttle, LH" - for 8+1 shifters: 8 gears, one button to change driving direction, one button to swtich between low and high range
* "4G, R+/-, 1R"- gears 1 to 4 change the highes 4 gears, gear 5 and 6 increase/decrease the range, gear 7 switches to reverse gear
* "4G, R+/-, Shuttle" - gears 1 to 4 change the highes 4 gears, gear 5 and 6 increase/decrease the range, gear 7 toggles the driving direction
* "4G, R+/-, D/R" - for 8+1 shifters: gears 1 to 4 change the highes 4 gears, gear 5 and 6 increase/decrease the range, gear 7 switches to forward, gear 8 switches to backward
* "D/R , G+/-, R+/-" - gear 1 swtiches to forward, gear 2 switches to backward, vehicle is in neutral in neither 1 nor 2 are pressed, gears 3 and 4 change the gear, gears 5 and 6 change the range

The IVT transmission has now two different ranges. The default should be the high range.

## modSettings
I renamed the configuration file in modSettings folder to just "config.xml". Additionally, there is a new file "transmissions.xml". Here you can add your own transmissions. I propose to use the second transmission as template. Gears support automatic shifting. but ranges have to be shifted manually. 

## VehicleControlAddon is the new KeyboardSteer
Please check section status why I renamed the mod. Please use VCA as abbreviation.

You will have to choose the new mod after replacing it in the mods folder. But settings in old save games are still read.

## Developer version
Please be aware you're using a developer version, which may and will contain errors, bugs, mistakes and unfinished code. 

You have been warned.

If you're still ok with this, please remember to post possible issues that you find in the developer version. 
That's the only way we can find sources of error and fix them. 
Be as specific as possible:

* tell us the version number
* only use the vehicles necessary, not 10 other ones at a time
* which vehicles are involved, what is the intended action?
* Post! The! Log! to [Gist](https://gist.github.com/) or [PasteBin](http://pastebin.com/)

From today on I will close all new issues without the above information!

## Motivation
Although I have a steering wheel, but almost always play with the keyboard. On winding roads, I am again and again landed in the ditch in front of nights or power poles.

## Description
This script varies the steering speed depending on the speed you are driving, and it rotates the camera to match the steering angle and direction.
Shift-Left limits throttle, cruise control and maximum rounds per minute to 75%. With Shift-right and the cursor keys you can peek in the corresponding direction.
If you press Ctrl left together with W then the driving direction snaps to fixed directions.
Additionally, there is a simple gear box. It was never planned to make a super realistic gearbox. The following transmisions are available:
* off: the standard gearbox without customization
* IVT: Still the standard gearbox but with little adjustments to the allowed RPM range. More to come...
* 4X4: An old fashioned transmissoin with 4 gears in 4 groups and shuttle control. Shifting gears takes time and you might lose momentum.
* 4PS: The same transmissoin as above but with power shift for the gears
* 2X6: Two groups with 6 gears. This transmission is useful for G27/G29 gear shifters. There is a low and a high range. The 6 gears in each range do not overlap with the 6 gears in the other range
* FPS: Full Power Shift: The transmission has 12 gears and shifts without interuption. 
* 6PS: 6 gears with power shift: This transmission has 6 gears. Each gear can be reduced by about 80%

All functions are switchable with the following default key combinations:
* Ctrl Left + C: Settings
* Ctrl Left + W: Snap Angle (continue)
* Alt Left + W: Snap Angle (reset)
* Shift Left: Throttle limiter / reduced cruise control speed
* Shift Right + Cursor: look forward, backwards, left right
* Space: Change direction (aka shuttle control)
* Please check the keys for shifting. G27/G29 gear shifters are supported.
* The 7th gear of the gear shifter is special. If you use action binding ksmShifter7 please make sure that shuttle control is enabled. This action binding will swtich into 1st reverse gear. 
* Best transmission in combination with a gear shifter are 2X6, FPS and 6PS. 

## Developer version
Please be aware you're using a developer version, which may and will contain errors, bugs, mistakes and unfinished code. 

You have been warned.

If you're still ok with this, please remember to post possible issues that you find in the developer version. 
That's the only way we can find sources of error and fix them. 
Be as specific as possible:

* tell us the version number
* only use the vehicles necessary, not 10 other ones at a time
* which vehicles are involved, what is the intended action?
* Post! The! Log! to [Gist](https://gist.github.com/) or [PasteBin](http://pastebin.com/)

## Credits
* Stefan Biedenstein
