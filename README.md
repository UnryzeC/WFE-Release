# WFE - Warcraft Feature Extender

![WFE_Main_Picture](https://user-images.githubusercontent.com/95709901/154843938-b174a754-64f2-4f9d-90fe-bab9be178aab.png)

## Contents
- [About](#about)
  - [Supported patches](#supported-patches)
  - [Additional download URLs](#additional-download-urls)
- [Features](#features)
- [How to use](#how-to-use)
  - [Method 1](#method-1)
  - [Method 2](#method-1)
- [Credits](#credits)
- [FAQ](#faq)

## About

Reserved for in-depth explanation...

### Supported patches
* 1.24e
* 1.26a
* 1.27a
* 1.27b
* 1.28f

### Additional download URLs:

* [Google](https://drive.google.com/drive/folders/1iqKaNc6qL_aTRRBuUH0r_OGBLT9Rr0_S?usp=sharing)
* [Yandex](https://disk.yandex.ru/d/ZGbj4W15kamRMg)
* Yandex: https://disk.yandex.ru/d/ZGbj4W15kamRMg

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

#### 2. Launch WFE.exe and choose desired parameters and click Save:

* Default config settings are saved in WFEConfigBase.ini

![WFE_Config_Base](https://user-images.githubusercontent.com/95709901/154843693-ffbf08bb-b8b5-4fba-93b5-528632fbf294.png)

If WFEConfig.ini is not present, WFE will use it as a main config file instead.

* If WFEConfig.ini is present or Save button was used to create WFEConfig.ini, then all the new parameters will be written to it.

![WFE_Config_Example](https://user-images.githubusercontent.com/95709901/154843696-f0229a09-e30e-42e7-9501-9885975c03b6.png)

#### 3. Setting up Path to the Game:

* Patches below 1.28.

![WFE_Game_Path_Pre_1 27b_Option](https://user-images.githubusercontent.com/95709901/154843688-908b80b4-8a5c-4651-b94b-0f618fd14788.png)
* Patches above 1.27b.

![WFE_Game_Path_Post_1 27a_Option](https://user-images.githubusercontent.com/95709901/154843687-9bb361ef-ff0f-40d2-b8ba-1e2cec801859.png)
* For EuroBattle.net/w3l.exe using platform.

![WFE_Game_Path_Custom_Launcher_Option](https://user-images.githubusercontent.com/95709901/154843686-6f3cf12c-4fb1-4e19-b032-1d641e9c8900.png)

Note: this is not mandatory, if you don't want to use WFE.exe as a launcher, as you can simply inject/use auto-injector to activate WFE library instead.

#### 4. Setting up Injector.

Note: do not let the name scare you, as WFE.exe needs to know what game to find and inject library to. This is an important step, so please read carefully!

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
#### 1. Extract all files to the MAIN folder of Warcraft 3 as shown on screenshot below.

![WFE_Extract_To_Folder](https://user-images.githubusercontent.com/95709901/154843697-879e295a-0f06-45f1-ad18-8f69f10dc695.png)
#### 2. Launch WFE.exe and choose parameters you desire and then push Okay to save changes to conf.ini or simply edit conf.ini directly.

![WFE_Config_Example](https://user-images.githubusercontent.com/95709901/154843696-f0229a09-e30e-42e7-9501-9885975c03b6.png)
#### 3. Launch Warcraft 3 and enjoy!

## Credits

* Karaul0v - for the initial tool called Quickcast, from which everything started and for helping me with many questions that I had.
* ENAleksey - for RenderEdge source code, from which I've taken many ideas and also for assisting me on some issues.
* Tomoya...Aki
* Bergi_Bear
* quq_CCCP
* VladBmw530 - bug reports and tests.
* And to all users for using my tool!

## FAQ

TBD




