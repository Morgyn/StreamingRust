# How to Protect Yourself While Streaming Rust

*"This is a game about information"* -[Ramsey](https://www.youtube.com/watch?v=YdYmtFbQ8mU&t=49s)

## Contents
1. [Introduction](#Introduction)
1. Friends
1. Streamer Mode
1. Protect your steam account
1. Hide your map
1. Clear your console
1. Hide the game
1. In-game chat and global messaages
1. Avoid non-vanilla servers
1. Voice
1. [Advantages of Facepunch run servers](#Advantages of Facepunch run servers)
1. Handy Binds

## Introduction
This is a guide on how to try and avoid getting streamsniped on rust. These are a list of steps you can take to try and mitigate people finding which server you are on and ruining your day. Information can be leaked very easily but most ways can be mitigated and it's entirely possible to avoid most attempts. However if someone has enough time and enough patience they can find you via brute force, so no methods are infalible.
## Friends
If a group of you are streaming, all of you must take the same steps. It's trivial to see who else is streaming, who's taking the least precautions and use them to find the group. If people aren't streaming, still ask them to take most of the [LINK HERE](steam profile precutions) and use streamer mode, so they don't call out peoples real steam profile names.
## Streamer Mode
  Streamer mode hides certain elements of the game, changing names and removing a few other identifiable features. Enable these settings before joining a server or starting your stream. Do not broadcast your Rust game before setting these, if you forget change them in another scene or with an overlay.
  
  In Options, set Streamer Mode ON and Rich Presence OFF
  ![Streamer Mode Options](https://github.com/Morgyn/StreamingRust/raw/main/streamermode.png)
  
  Or this can be enabled in console with:
  ```
  global.streamermode true
  global.richpresence false
  ``` 
  
  Other than the name changes, the largest change to your experience will be the Respawn/Bag screen. This screen will now be black with no map showing until you hit your map key. It's a change from the the normal experience but allows your [map hider](#Hide your map) to work on this as well. Follow the link for details on map hiding.
  
  Streamer mode will not help you with the following and you should [hide the game](#Hide the game):
  
  When giving a bag to someone their actual steam names will be shown, if you have given someone an alias this will be shown instead. Thankfully steamids are now hidden with streamermode, but you should still hide this screen as steam names of other players will be shown and the server can still be determined.
  
  The drone system currently has no protection for hiding the map, so hide the game before using.
  
  Harvesting bodies the skull will say ```Skull of STREAM_NAME``` irrespective of streamermode. Either don't harvest bodies or hide the game when interacting with the skull or body.
  
## Protect your steam account
 Make sure you're offline
 Hide your friends list
 Generic Icon
 Private your profile
 
## Hide your map
   OBS Studio
   SLOBS
   
## Clear your console
  ![Connection Message](https://github.com/Morgyn/StreamingRust/raw/main/Connecting.png)
  ![Size and Seed](https://github.com/Morgyn/StreamingRust/raw/main/sizeandseed.png)
  Replace F1 with clear
    Because server leaks, connection message, seed & mapsize, killed NAME (STEAMID)
  Discuss how top open the log to check things if cleared
  
## Scene to hide sensitive tasks like looking at your log.
  Bind Real Console to this scene
  F7 to switch scenes for reporting
  Drones
  Skulls
  
## Hide in game chat and globals
## Avoid non-vanilla servers
## Advantages of Facepunch run servers.
## Handy Binds

`bind u "console.clear;consoletoggle;combatlog"`
`bind q "forward;sprint"`
`bind f1 "console.clear;consoletoggle"`

  Voice Mute Toggle
`bind j "~audio.voices 5;audio.voices 0"`
 Change the 5 to whatever you normally use, and it will toggle between mute and normal volumes on press.

