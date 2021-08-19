This repository contains a modified version of [gompocp´s mods](https://github.com/gompocp/ActionMenuApi) for VRChat. 

+ Join the [VRChat Modding Group discord](https://discord.gg/rCqKSvR) for more mods!
+ Join the [VRCMG Unchained discord](https://discord.gg/boycottknah) for support and more mods!
+ Join the [VRC Modding Group Plus+](https://discord.gg/2k6pXM4uYw) for support

Using a modified MelonLoader without some security features brings a risk with it, you should read Knah's blogpost: [Malicious Mods and you](https://github.com/knah/VRCMods/edit/master/Malicious-Mods.md)

Don't blame me or other when you data or tokens get stolen. Always think about what mods you are using and why they are obfuscated and so on. 

Don't hatespeech the original Author please, without them this would not be possible!

# Disclaimer

Modding the VRChat client is against VRChat's Terms of Service. Therefore use these mods at your own risk. I am not responsible for if you get banned or any other punishment by using these mods!<br>

## Mods
<ol>
  <li><a href="#actionmenuapi">ActionMenuApi</a></li>
  <li><a href="#actionmenuutils">ActionMenuUtils</a></li>
  <li><a href="#downloadfix">DownloadFix (Depracated)</a></li>
<li><a href="#standalonethirdperson">StandaloneThirdPerson</a></li>
  <li><a href="#worldpredownload">WorldPredownload</a></li>
  
</ol>

## Canny Posts



I highly recommend checking out the canny posts linked below and upvoting if you'd like VRChat to implement some mods as actual vanilla features
* [World Predownloading/Preloading](https://feedback.vrchat.com/feature-requests/p/preload-worlds)
* [Menu Respawn Issue ActionMenuUtils addresses](https://feedback.vrchat.com/feature-requests/p/respawnhub-hotkey)
* [Not currently a mod feature but priority for friend's avatars first](https://feedback.vrchat.com/feature-requests/p/friends-first-model-priority-loading)
* [Thirdperson for Keyboard/Mouse Users](https://feedback.vrchat.com/feature-requests/p/thirdperson-for-keyboardmouse-users)

## Building

To Build simply
1. Clone repo using git
2. Open solution in an ide that supports C#
3. Inside `Directory.Build.props` edit the path inside `<VRChatFolder>` to the path of your own game install
4. Build Solution

## ActionMenuApi

This mod doesn't do anything on it's own. <br>
It provides an easy way for modders to add integration with the action menu. <br>
It supports the use of the <br>
* Radial Puppet
* Four Axis Puppet
* Button
* Toggle Button
* Sub Menus

Additionally allows mods to add their menus to a dedicated section on the action menu to prevent clutter. <br>
More information [here](https://github.com/gompocp/ActionMenuApi)

## ActionMenuUtils 
- Lets you respawn using the action menu<br>
- Lets you go home for when respawning wont save you such as in broken worlds with no floor<br>
- Additionally lets you reset avatar or rejoin instance<br>
- Shows an example of how you might use my action menu api thingy :) more info available [here](https://github.com/gompocp/ActionMenuApi/) <br>


### Acknowledgements
- [Knah](https://github.com/knah/) for the assetbundle loading mechanism from https://github.com/knah/VRCMods,<br>
  for suggesting to add a button for go home and just help in general :)
- [Ben](https://github.com/BenjaminZehowlt/) for xref scanning mechanism from https://github.com/BenjaminZehowlt/DynamicBonesSafety
- SOS emoji from https://openmoji.org/ full credit to them for it


## DownloadFix

> The bug this mod aimed at helping with has now been patch in Build 1106+. Therefore there's no reason to use this mod anymore :) 

- Yeah its literally a one line fix for the loading bug  <br>
- Adds a button to the UIX settings page and to the world loading screen <br>
- Don't really know what else to say about it so yeah <br>


## StandaloneThirdPerson
- KeyBind configurable via uix/the config file. Valid values can be found [here](https://docs.unity3d.com/ScriptReference/KeyCode.html) (exluding `None`)
- Third person camera fov and nearclipplane value can be edited as well via uix/the config file

### Acknowledgements
- Credit to [Knah](https://github.com/knah/) for [EnableDisable Listener](https://github.com/knah/VRCMods/blob/master/UIExpansionKit/Components/EnableDisableListener.cs)
- Credit to [Psychloor and emmVRC team](https://github.com/Psychloor/PlayerRotater/blob/master/PlayerRotater/Utilities.cs#L76) for world check
- Credit to [ljoonal](https://github.com/ljoonal/) some of the math is loosely based off of their [third person mod for cvr](https://github.com/ljoonal/CVR-Mods/blob/main/ThirdPersonCamera/ThirdPersonCamera.cs)
- Some acknowledgement needs to be given to [emmVRC](https://github.com/emmVRC/) as they are the people that originally (afaik ¯\\\_(ツ)_/¯ ) had a third person mod for vrchat

## WorldPredownload<br>
- You can hit preload on an invite, on a world page or on a friend user page
- You can see your download status bottom right of quick menu
- Currently you can only download/preload one world at a time
- If you go to another world while downloading, it'll cancel the download
- Performance may degrade for split second on world enter due to you having a large cache size

### Acknowledgements
- Credit to [Psychloor](https://github.com/Psychloor/AdvancedInvites/blob/master/AdvancedInvites/InviteHandler.cs) for method to convert worldID to apiWorld instance + much much more, and some of the way stuff is structured is also inspired by his utilities file
- Credit to [Ben](https://github.com/BenjaminZehowlt/DynamicBonesSafety) for xref scanning mechanism and hud icon idea
- Credit to [Knah](https://github.com/knah/) for [Enable Listener](https://github.com/knah/VRCMods/blob/master/UIExpansionKit/Components/EnableDisableListener.cs) and the [hud icon method](https://github.com/knah/VRCMods/blob/master/JoinNotifier/JoinNotifierMod.cs#L120) that I changed to use here along with the [assetbundle loading mechanism](https://github.com/knah/VRCMods/blob/master/JoinNotifier/JoinNotifierMod.cs#L61)
- fwenny for helping with some testing 

Repo structure from [Knah's VRCMods Repo](https://github.com/knah/VRCMods/)
