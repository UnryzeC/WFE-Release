# WFE - Warcraft Feature Extender

![WFE_Main_Picture](https://github.com/user-attachments/assets/99a494ed-93e4-4aa6-8929-ef67d72dfa03)

## Contents
- [About](#about)
  - [Supported patches](#supported-patches)
- [Features](#features)
- [How to use](#how-to-use)
  - [Method 1](#method-1)
  - [Method 2](#method-1)
- [Credits](#credits)
- [FAQ](#faq)
- [Contacts](#contacts)
- [Want to donate?](#want-to-donate-?)

## About

Reserved for in-depth explanation...

### Supported patches
* 1.24e
* 1.26a
* 1.27a
* 1.27b
* 1.28f

## Features
* Live updating options, without the need of relaunching the game!
* Possibility of adding your own language to language.xml.
* Autocast (hold the button and it will repeat itself).
* Smartcast setting for every single button separately.
* FPS limit removal (contains two options).
* Hotkey setting for abilities/items and combination hotkeys!
* Camera 360 degree incline control with mouse wheel (Hotkey can be added).
* Camera height control with CTRL hotkey + mouse wheel (Hotkey can be changed).
* Camera rotation control with ALT hotkey + mouse wheel (Hotkey can be changed).
* Camera step setting for Camera modifications mentioned above.
* Mouse lock.
* Widescreen support.
* BLP 512x512 limit removal.
* Single Player pause removal.
* Delay setting for Single Player/LAN/Battle.net.
* Delay setting for game start for LAN.
* Map size limit removal. (Removes map size restriction for online hosting/joining).
* Detailed information of movement speed and attack speed.
* HP/MP regeneration display (only displays yours and allies).
* Right mouse button click repeater (delay can be set in option "Action").
* Enforce Hotkey option. (This overrides default WC3 hotkeys).
* Manabar.
* Healthbar colour control (Your/Ally/Enemy/Neutral).
* Display/Hide all UI.

## How to use

### Method #1:
#### 1. Extract all files to desired folder:

![WFE_Extract_To_Folder](https://user-images.githubusercontent.com/95709901/154843697-879e295a-0f06-45f1-ad18-8f69f10dc695.png)

Note: I strongly advice to extract WFE to a SEPARATE folder, as it prevents any possible collisions with other applications that may read/access any of the WFE files.
Example: When WFE is in root Warcraft 3 folder, test commands won't work as for some reason Localisation and TestCommands are being accessed by it, probably as the game tries to read any .ini files, hence creating the issue.

#### 2. Launch WFEApp.exe:

* Rename WFEConfigBase.ini to preferred one in the Profile field:

![image](https://github.com/user-attachments/assets/0333114f-2aab-4844-b768-9f208248b89e)

* Now click "+" this will generate profile:

![image](https://github.com/user-attachments/assets/4cde1e45-fc9c-41d7-841c-abc55656aaf2)

* Now clicking Save will generate/update YOUR_PROFILE_NAME.ini in the Profiles folder:

![WFE_Config_Example](https://github.com/user-attachments/assets/58524265-705b-414b-9d29-f648f834ff45)

Any subsequent Save clicks will simply update this file and update settings in-game.

#### 3. Setting up Path to the Game:

* Patches below 1.28.

![WFE_Game_Path_Pre_1 27b_Option](https://user-images.githubusercontent.com/95709901/154843688-908b80b4-8a5c-4651-b94b-0f618fd14788.png)
* Patches above 1.27b.

![WFE_Game_Path_Post_1 27a_Option](https://user-images.githubusercontent.com/95709901/154843687-9bb361ef-ff0f-40d2-b8ba-1e2cec801859.png)
* For EuroBattle.net/w3l.exe using platform.

![WFE_Game_Path_Custom_Launcher_Option](https://user-images.githubusercontent.com/95709901/154843686-6f3cf12c-4fb1-4e19-b032-1d641e9c8900.png)

Note: this is not mandatory, if you don't want to use WFEApp.exe as a launcher, as you can simply inject/use auto-injector to activate WFE library instead.

#### 4. Setting up Injector.

Note: do not let the name scare you, as WFEApp.exe needs to know what game to find and inject library to. This is an important step, so please read carefully!

##### 4.1 Configuring Process Name:

* For versions below 1.28, leave the name as is, aka war3.exe.

![WFE_Process_Name_Pre_1 27b_Option](https://user-images.githubusercontent.com/95709901/154843691-c2e3d73e-5150-4a61-bf71-7b27efca3ed5.png)
* For version above 1.27b, write Warcraft III.exe instead of war3.exe.

![WFE_Process_Name_Post_1 27a_Option](https://user-images.githubusercontent.com/95709901/154843689-069ed544-8d50-4ae7-9802-4ca4b7039dc0.png)

##### 4.2 Additional Libraries:

![WFE_Additional_Libraries_Path](https://user-images.githubusercontent.com/95709901/154843692-11057f57-fffb-4ff9-bd25-3b639621f292.png)

WFE will load from the specified folder any .dll/.mix files and inject them along the main library, this allows to de-clutter root Warcraft III folder, and well, load things in a simpler manner overall.

Note: this is not a mandatory option and you do not have to set a path inside of the WFE folder, but it's just easier and "more robust" to do so.

#### 4.3 Auto Injector:

When this option is enabled, it will use Delay (ms) time to re-scan processes until war3.exe/Warcraft III is found (based on the input Process Name). When found, if it did NOT inject main library to it yet, it will use the DLL Name to find main library (default: WFEDll.dll) and load it along with anything specified in the Additional Libraries if "Load Additional Libraries" option was selected.

##### 4.4 Auto-Inject:

This is only relevant if you are using "Launch" button, as it will automatically inject main library, without needing to do an extra click on "Inject" button.

### 5. Launching the game.

#### 5.1 Classic Method:

If Auto Injector IS NOT enabled:
* Simply launch the game as usual and use "Inject" button.

If Auto Injector is enabled:
* Simply launch the game as usual.
Note: as mentioned in Auto Injector, WFE.exe will inject the library itself.

#### 5.2 Launch Method:

If Auto-Inject IS NOT enabled:
* Click on "Launch" button.
This will launch the game from the specified path in the Game Path.

* Click "Inject" button.
This will inject main library to the specified Process from Process Name.

If Auto-Inject IS enabled:
1) Click on "Launch" button.
This will launch the game from the specified path in the Game Path.
Auto-Inject will inject main library to the specified Process from Process Name on its own.

#### 6. Updating Settings:

* Select/Change any necessary parameters in the program.
* Click Save.
This will update data in config and in-game.
You don't have to click Inject again.

### Method #2:
#### 1. Extract all files to the MAIN folder of Warcraft 3.
#### 2. Launch WFE.exe and choose parameters you desire and then push Okay to save changes to conf.ini or simply edit conf.ini directly.

![WFE_Config_Example](https://user-images.githubusercontent.com/95709901/154843696-f0229a09-e30e-42e7-9501-9885975c03b6.png)
#### 3. Launch Warcraft 3 and enjoy!

## Credits

### Creator/Developer:
* Unryze (me) - creating and maintaining WFE.

### Special thanks to:
* Karaul0v - for the initial tool called Quickcast, from which everything started and for helping me with many questions that I had.
* ENAleksey - for RenderEdge source code, from which I've taken many ideas and also for assisting me on some issues.

### Testers:
* Andutrache
* Yeran
* quq_CCCP
* Tomoya...Aki
* JackFastGame
* Ham5terzilla
* Karolson
* MalcolmRU
* Bergi_Bear
* VladBmw530
* Dam3w
* S_Prince_A
* GoodlyHero
* ThisName232
* Падиниц
* AshtonLee
* Artwork_DT
* Vinsera

### Translators:
* Moon (Swedish)
* DSY (German)
* Artwork_DT (Vietnamese)
* EdgarL (Chinese)

## FAQ

## Keys Section

#### What is SmartCast?
    This is a feature that will automatically issue Left Mouse Click when any ability/attack/move or active item is pressed.

#### What is Self Cast Hotkey?
    This is essentially an additional Hotkey, which while being held, will cause your next ability/attack/move or active item Hotkey to be cast on you/underneath you.

#### What is AutoCast toggle Key?
    This is an additional HotKey, which while being held, will switch Autocast toggle on an ability, such as flaming arrow/frost arrows/frost armour and so on.

#### What is AutoCast Mouse Delay?
    This is a setting that allows you to configure XButton1 and XButton2 repeat delay (these are additional side buttons on a mouse).

#### What is Hero Only in Keys Section?
    This option will make WFE Keybinds to only work on Units of type Hero.

## HotKeys Section
### Utility:

#### What is Update Data?
    This will simply update your saved configuration for the WFEDll.dll, it will also update it in-game.

#### What is Window/Borderless?
    This option will toggle between Window mode and Borderless Window mode, if game was launched with '-window' attribute.

#### What is Mouse Lock On/Off?
    This toggles Mouse Lock, meaning it turns it on or off.

#### What is Widescreen On/Off?
    This allows you to toggle Widescreen, meaning you can turn it off or on.

#### What is Pause On/Off?
    This toggles Disable Single Player Pause Feature.

#### What is UI Hide/Show?
    This toggles whole UI on and off.

#### What is Toggle Multiboard State?
    This maximises/minimises Multiboard.

#### What is Show/Hide Multiboard?
    This shows/hides Multiboard.

#### What is Clear Messages?
    This clears all Messages (trigger messages) from screen.

#### What is Clear Chat Messages?
    This clears all chat messages from screen.

### Camera:

#### What is Override?
    This makes WFE take control of the game camera, hence making any changes to the camera from the map disabled.

#### What is Restore?
    This restores default camera settings, such as Height, Angle of Attack and so on.

#### What is Distance?
    This Hotkey while being held, if mousewheel is used or +/- keys, will increase/decrease camera's distance from the map.

#### What is Height?
    This Hotkey while being held, if mousewheel is used or +/- keys, will increase/decrease camera's height.

#### What is Incline?
    This Hotkey while being held, if mousewheel is used or +/- keys, will increase/decrease camera's Angle of Attack (position vertically around the map).

#### What is Rotation?
    This Hotkey while being held, if mousewheel is used or +/- keys, will increase/decrease camera's Rotation (position horizontally around the map).

### Unit:

#### What is Save?
    This saves currently selected unit in library's memory.

#### What is Select?
    This will re-select unit that was saved in library's memory.

#### What is Autoselect On/Off?
    This toggles automatic re-selection of unit that was saved in library's memory.

#### What is Clear Selection?
    This will clear Selection UI from any selected units.

### Custom Indicators:

#### What is Draw Attack on hover?
    This will draw Attack Range Indicator when mouse is hovering over Attack Icon and set Hotkey is pressed.

#### What is Draw Attack?
    This will draw Attack Range Indicator when set Hotkey is pressed.

#### What is Draw Spell AoE on hover?
    This will draw Ability/Spells's Range/AoE Indicator when mouse is hovering over it and set Hotkey is pressed.

#### What is Draw Bound Spell?
    This will draw Ability/Spells's Range/AoE Indicator when custom Hotkey for that Ability/Spell is pressed and set Hotkey is pressed.

#### What is Draw Sight Radius?
    This will draw unit's Sight Range Radius Indicator when set Hotkey is pressed.
===============================================

### Settings Section

#### What is Widescreen?
    This is a feature to change 4:3 perspective to a 16:9 for modern systems.

#### What is AutoCast?
    This is a feature that will continiously repeat the button that is being held. Meaning, if you hold Q, it will be repeated until it's being held.

#### What is Mouse Lock?
    This option will lock the mouse from going out of the Warcraft III window, however this will only do so if you are in game, not in menu and so on.

#### What is Save to WC3 Folder?
    This is legacy feature, for those, who still use Method 1 (.mix library) for some reason. This will copy WFE config to Warcraft III folder.

#### What is Detailed Attack Tip?
    This will extend the information in the Attack Tooltip, adding precise numbers to Attack Speed and Attack Cooldown.

#### What is Extended Attack Tip?
    This will further extend the information in the Attack Tooltip, which will separate the total value of any stat into base and additional stat, aka white and green.

#### What is Detailed Defense Tip?
    This will extend the information in the Defense Tooltip, adding precise movement speed value and sight radius.

#### What is Extended Defense Tip?
    This will further extend the information in the Defense Tooltip, which will separate the total value of any stat into base and additional stat, aka white and green.

#### What is HP Regen?
    This will draw your selected unit's Health Regeneration near its Health number.

#### What is MP Regen?
    This will draw your selected unit's Mana Regeneration near its Mana number.

#### What is Write Magical Resist?
    This prints Magic Resist into Defense tooltip.

#### What is Enforce Hotkeys?
    This makes WFEs Hotkeys have a higher priority over overlapping Game's Hotkeys.

#### What is Unlock Map Size?
    This simply removes 4 MB (on patches prior to 1.26a) and 8 MB map limit from Online Hosting.

#### What is Disable Pause?
    This disabled the pause in Single Player, when you alt-tab from the game, or have Warcraft III window minimised.

#### What is Remove BLP Limit?
    This removes the 512x512 BLP limit, allowing any texture in BLP above 512x512 to avoid down-scaling, hence avoiding quality loss.

#### What is Loading Notification?
    This will put Warcraft III window as current active window, if the game has started and the game was minimised or put to background.

### Health Colours:
    This will hook all unit's Health Bars and allow customisation based on selected choices.

#### What is Height?
    This sets the height of the Health Bar.

#### What is Your/Ally/Enemy/Aggressive/Passive?
    This sets colours for each selected alliance.

### Mana Bara:
    This will additionally draw a Mana Bar for each unit. Note: this won't work correctly if library is injected after the game has already started, it should be done in loading or on game start up.

#### What is Height?
    This sets the height of the Mana Bar.

#### What is Hero Only?
    This will make Mana Bar to be only drawn for Heroes.

#### What is Colour?
    This sets the default colour of Mana Bar.

### Cooldown UI:
    This adds numerical cooldown indicators to Abilities/Items/Units. Meaning it will display cooldown and stock charge.

#### What is Show Indicator?
    This sets the visibility of the cooldown model's visibility (the circular shadow animation) to be visible or hidden.

#### What is Display Minutes?
    This will show cooldown using minutes and seconds, instead of just seconds. Example: 70 seconds will be drawn instead as 1:10.

#### What is Refresh Time?
    This sets the time that WFE will re-check all the cooldowns and update those values.

#### What is Text?
    This sets the colour of the text for cooldown indicator.

#### What is Shadow?
    This sets the border colour around the text.

### Repeat Right Mouse Click:
    This option simply repeats Right Mouse Click while it's being pressed.
    
#### What is Delay(ms)?
    This sets the delay before the next press is repeated.

### Delay (ms):
    This contains the latency settings for LAN/Battle.net and delay for Game Start. All of these only take effect if you are the host.

#### What is LAN?
    This sets the latency for games that you host in Local Area Network.

#### What is Battle.net?
    This sets latency for games hosted using Battle.net or any other PVPGN option.

#### Why is there no Single Player setting?
    This value is taken directly from LAN, since there is no real point in having it as a separate value.

#### What is Game Start?
    This is the count down time before the game begins.

#### Display:
    This contains settings for FPS Limit and FPS Unlocker method.

#### What is Status?
    This is a setting for the unlocking method. New - more aggressive and yields higher framerate. Legacy - softer method and stresses CPU less.

#### What is FPS Limit?
    This sets the upper ceiling for the framerate, however it is no longer really relevant, the higher - the better.

#### What is Refresh Rate?
    This sets the upper ceiling for the refresh rate, meaning it will tell DirectX8/9 the rate at which your monitor is being refreshed.

### Camera Steps:
    This option when turned on will allow WFE to modify camera values with the input settings as steps.

#### What is Distance/Height/Incline/Rotation?
    These are set values for the Camera Modification via special Hotkeys.

#### What is FarZ?
    This is the maximum distance for the camera height perspective, the black "cut" when camera is near its edge.

#### What is FogZ?
    This is the height of the fog, that offsets the brightness of the camera's view, depending on how close it is to it.

### Custom Indicator Colours:
    This option when turned on, will allow Custom Indicator Draw and will also set a colour to them based on the colours that were selected.

#### What is Attack?
    This will set the colour of Attack Range Indicator.

#### What is Draw Spell AoE ?
    This will set the colour of Ability/Spells's Range/AoE Indicator.

#### What is Draw Sight Radius?
    This will set the colour of unit's Sight Range Radius Indicator.

#### Damage Draw:
    This option when turned on, will create TextTags with the damage that unit has received.

#### What is Physical Colour?
    This sets the colour for any damage that was dealt from a normal attack.

#### What is Physical Offset?
    This sets the horizontal position for the text from unit for a normal attack damage.

#### What is Magical Colour?
    This sets the colour for any damage that was dealt from spells/trigger damage or anything that is not a normal attack.

#### What is Magical Offset?
    This sets the horizontal position for the text from unit for a magical attack damage.

#### What is Height?
    This sets the height that drawn text has to reach.

#### What is Speed?
    This sets the speed that drawn text travels at.

#### What is Duration?
    This sets the duration that drawn text exists for.

#### What is Angle?
    This sets the angle that drawn text travels to.

#### What is Size?
    This sets the size of the drawn text.

#### What is Hero Only?
    This will only draw damage, if unit that received damage is of the Hero type.

#### What is All/Enemy/Ally/My?
    This sets alliances for which units should the text be drawn.

## Interface Section

### Enable UI Modification:
    This when turned on will edit Warcraft III game UI with selected options.

#### What is Black Bars?
    This shows/hides the Black Bars at top and the bottom of the Game UI.

#### What is Info Bar?
    This shows/hides unit's information, such as Attack Info Icon, Main Stat and Defense. Along with some other stuff.

#### What is Console?
    This shows/hides the overlay that contains every other button. (This only shows/hides the overlay).

#### What is Resource Bar?
    This shows/hides the resource icons and their information.

#### What is Upper Menu Bar?
    This shows/hides Info/Menu/Message log and other buttons.

#### What is Ability Buttons?
    This shows/hides all unit's ability buttons, this does not break their functionality.

#### What is Hero Icons?
    This shows/hides all the icons of heroes that are drawn on the left, this does not break their functionality.

#### What is Item Buttons?
    This shows/hides all the item buttons, this does not break their functionality.

#### What is Minimap?
    This shows/hides Minimap.

#### What is Minimap Buttons?
    This shows/hides all the buttons that are connected to Minimap.

#### What is Portrait?
    This shows/hides unit's portrait model.

#### What is Inventory Cover?
    This shows/hides the cover for the inventory for units that do not have item slots.

#### What is Peon Icon?
    This shows/hides the button for idle workers, this does not break it's functionality.

#### What is Time Indicator?
    This shows/hides time indicator at the top center.

#### What is Tooltip?
    This shows/hides the tooltip frame.

#### What is Mouse Tooltip?
    This attaches the tooltip to the mouse, instead of drawing it in the bottom right corner.

## Messages Section
- Honestly speaks for itself.

## Launcher Section

### Game Settings:

#### What is Game Path?
    This sets the path to the game, so it can be launcher with "Launch" button.

#### What is Launch Arguments?
    This sets the arguments with which the game will start, such as -window and so on.

#### What is Borderless?
    This will launch the game in borderless windowed mode, if the game was launched with -window argument.

### Window Settings:

#### What is Main Window Name?
    This is the so called Window Class, meaning the top-most name of the application.

#### What is Window Name?
    This is the actual name of the Window that is nested inside of the Window Class.

### Libraries Settings:

#### What is DLL Name?
    This sets the main library for the application to look for injection.

#### What is Auto-inject?
    This when enabled will automatically load and inject main DLL that is stated in DLL Name and Additional Libraries.

#### What is Additional Libraries Path?
    This points to a folder, from which all files with .dll/.mix/.asi will be automatically injected and loaded to the game if 'Auto-inject' is on.

## Registry, errors and other issues

### Warcraft III fatals on exit?
    Check Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows NT\CurrentVersion\AppCompatFlags\Layers and look for IgnoreFreeLibrary<Game.dll>. if it exists, remove this rule.

### What is Warcraft III registry path?
    Computer\HKEY_CURRENT_USER\Software\Blizzard Entertainment\Warcraft III

## Library doesn't work?

    Download x86: vc_redist.x86.exe from https://support.microsoft.com/en-us/topic/the-latest-supported-visual-c-downloads-2647da03-1eea-4433-9aff-95f26a218cc0
    Once installed, test it again.

## Contacts

- Discord: unryze
- VK: https://vk.com/unryze/
- VK Group: https://vk.com/unryzeworkshop/

## Want to donate?

Paypal: https://paypal.me/Unryze/
