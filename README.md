# How to Protect Yourself While Streaming Rust

*"This is a game about information"* -[Ramsey](https://www.youtube.com/watch?v=YdYmtFbQ8mU&t=49s)

## Contents
1. [Introduction](#Introduction)
1. [Friends](#Friends)
1. [Streamer Mode](#Streamer-Mode)
1. [Protect your steam account](#Protect-your-steam-account)
1. [Hide your map](#Hide-your-map)
1. [Clear your console](#Clear-your-console)
1. [Hide the game](#Hide-the-game)
1. In-game chat and global messages
1. Avoid non-vanilla servers
1. Voice
1. [Advantages of Facepunch run servers](#Advantages-of-Facepunch-run-servers)
1. Handy Binds

## Introduction
This is a guide on how to try and avoid getting stream-sniped on rust. These are a list of steps you can take to try and mitigate people finding which server you are on and ruining your day. Information can be leaked very easily but most ways can be mitigated and it's entirely possible to avoid most attempts. However if someone has enough time and enough patience they can find you via brute force, so no methods are infallible.

Remember, all information is additive. Something might seem a very unimportant bit of information but if this can be used to narrow down the server it's best not to let that information out for free.

## Friends
If a group of you are streaming, all of you must take the same steps. It's trivial to see who else is streaming, who's taking the least precautions and use them to find the group. If people aren't streaming, still ask them to take most of the [LINK HERE](steam profile precautions) and use streamer mode, so they don't call out people's real steam profile names.
## Streamer Mode
  Streamer mode hides certain elements of the game, changing names and removing a few other identifiable features. Enable these settings before joining a server or starting your stream. Do not broadcast your Rust game before setting these, if you forget to change them in another scene or with an overlay.
 
  In Options, set Streamer Mode ON and Rich Presence OFF
  ![Streamer Mode Options](/streamermode.png)
 
  Or this can be enabled in console with:
  ```
  global.streamermode true
  global.richpresence false
  ```
 
  Other than the name changes, the largest change to your experience will be the Respawn/Bag screen. This screen will now be black with no map showing until you hit your map key. It's a change from the the normal experience but allows your [map hider](#Hide-your-map) to work on this as well. Follow the link for details on map hiding.
 
  Streamer mode will not help you with the following and you should [hide the game](#Hide-the-game):
 
  When giving a bag to someone their actual steam names will be shown, if you have given someone an alias this will be shown instead. Thankfully steamids are now hidden with streamermode, but you should still hide this screen as steam names of other players will be shown and the server can still be determined.
 
  The drone system currently has no protection for hiding the map, so hide the game before using.
 
  Harvesting bodies the skull will say ```Skull of STEAM_NAME``` irrespective of streamermode. Either don't harvest bodies or hide the game when interacting with the skull or body.
 
## Protect your steam account
 ### Consider a dedicated Rust account
 ### Genericise your Steam name.
 ### Generic Icon
 ### Private your profile
 ### Make sure you're invisible
 ### Hide your friends list
 
## Hide your map
Hiding your map is important for a number of reasons. The locations of yourself, your teammates, your bags and of course your base. The map itself can leak the server, the various unique features of a map makes it while not trivial to find the map, easily lowers the number of possibilities, combined with other information this becomes trivial.

To configure a map hide, read the section that relates to your streaming software. At the moment only OBS Studio and StreamLabs OBS are included.

### OBS Studio
   OBS Studio requires additional software and a plugin. I've forked a copy of the software and have it available [here](https://github.com/Morgyn/OBSKeys). Please follow the projects instructions, it includes where to source the plugin.
### StreamLabs OBS
   The configuration of Streamlabs OBS is very easy, but it has a flaw that it leaks a few frames when you release the hotkey
   [StreamLabs OBS(/SLOBS Map Hide.md)
   
## Clear your console
  ![Connection Message](/Connecting.png)
  ![Size and Seed](/sizeandseed.png)
  ![Killed by message](/youdied.png)
  Replace F1 with clear
    Because server leaks, connection message, seed & mapsize, killed NAME (STEAMID)
  Discuss how top open the log to check things if cleared
 
## Hide the game
  Bind Real Console to this scene
  F7 to switch scenes for reporting
  Drones
  Skulls
 
## In-game chat and global messages
## Avoid non-vanilla servers
## Voice
## Advantages of Facepunch run servers.
## Handy Binds

`bind u "console.clear;consoletoggle;combatlog"`
`bind q "forward;sprint"`
`bind f1 "console.clear;consoletoggle"`

  Voice Mute Toggle
`bind j "~audio.voices 5;audio.voices 0"`
 Change the 5 to whatever you normally use, and it will toggle between mute and normal volumes on press.
