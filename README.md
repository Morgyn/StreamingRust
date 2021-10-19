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
If a group of you are streaming, all of you must take the same steps. It's trivial to see who else is streaming, who's taking the least precautions and use them to find the group. If people aren't streaming, still ask them to take most of the actions to [protect their steam account](Protect-your-steam-account) and use streamer mode, so they don't call out people's real steam profile names.
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
  
  Reporting someone with F7 will list players on the server with you, along with thier Steam IDs.
 
## Protect your steam account
Once someone has your steam account it's far to easy to find your friends and locate your server. It's trivial using your profile name to find the server you are currently on. Additionally while you are playing the game, if someone on your server realises you are streaming they can can turn into a stream sniper and also potentially inform other people that you are streaming.
 ### Consider a dedicated Rust account
 Having a dedicated steam account just for Rust will avoid most of the downsides of locking your account down and depersonalising it. If you are wanting to retain all the social aspects of your current steam account, I recommend a dedicated account.
 ### Genericise your Steam profile name.
 Your steam name is probably the most important part to change. It needs to be changed to something absolutely generic and common. You may want to make it a funny phrase or name, but this just makes you easier to find. Single short first names are great, Bob, John or Mary are examples. The more common the better. In game you're going to be using streamer mode anyway so your and your friends Steam profile names do not matter.
 ### Generic Icon
 The same applies to your Steam profile icon, it's no where near as important as your name but while playing someone recognises your icon when you kill them then they will have your steam profile and will be able to use that to snipe you from then on.
 ### Steam URL
 Having a vanity url with your streamer name makes it increadibly easy to find your profile.
 ### Comments
 Comments on your profile indicating you stream, or what your twitch is.
 ### Hide your friends list
 Always hide your friends list from everyone. You might inadvertantly leak other streamers profiles orr give people a chance to find who you are playing with and use them to find your server.
 ### Private your profile
 Privating your profile to everyone is the easiest option as it will hide your friends list and your comments, and any other information that may be on your profile.
 ### Make sure you're invisible
 If you set yourself to invisible you will appear as offline to everyone, set this before you play/stream. This will prevent your profile saying you are in Rust or even worse Rich Presence showing the exact server you are playing.
 ![Set steam to invisible](/goinvisible.png)
 
 
## Hide your map
Hiding your map is important for a number of reasons. The locations of yourself, your teammates, your bags and of course your base. The map itself can leak the server, the various unique features of a map makes it while not trivial to find the map, easily lowers the number of possibilities, combined with other information this becomes trivial.

To configure a map hide, read the section that relates to your streaming software. At the moment only OBS Studio and StreamLabs OBS are included.

### OBS Studio
   OBS Studio requires additional software and a plugin. I've forked a copy of the software and have it available [here](https://github.com/Morgyn/OBSKeys). Please follow the projects instructions, it includes where to source the plugin.
### StreamLabs OBS
   The configuration of Streamlabs OBS is very easy, but it has a flaw that it leaks a few frames when you release the hotkey
   [StreamLabs OBS(/SLOBS Map Hide.md)
   
## Clear your console
  Your console can easily leak the server and you should never show it on stream. Now that there is a suicide option on the main menu you should not need to use kill in console but old habits die hard. Sometimes you'll want to show combatlog or need it in the middle of action.
  
  The connection information is shown when you connect to a server by default and looks like this:
  
  ![Connection Message](/Connecting.png)
  
  After that, while it looks innocuous the seed and map size is enough to find the server in most cases.
  
  ![Size and Seed](/sizeandseed.png)
  
  Every time you die there is a "You died" message. This will contain the real steam name (no streamermode name) and the steam id in square brackets. Either of these bits of information makes finding the server trivial. Even worse, if you commit suicide, your steam id is shown.
  
  ![You died](/youdied.png)
  
  To remedy this I suggest changing the default F1 console bind to a bind that clears the console first.
  
  ```
  bind f1 "console.clear;consoletoggle"
  ```
  
  You can bind another key to a non cleared console and make this key a hotkey in obs for your [hide the game](#Hide-the-game) method
  
  If you need to check your log for any reason, you can click "LOG FILE" from the console. This will open the log file in notepad. There is a lot of debug information in there, but all console messages such as the "You died" are logged there. You can use notepad's search function to find these events quickly.
  
## Hide the game

  Some parts of the game will leak information no matter what, but you can take some steps to avoid this by hiding the game briefly while doing this task. This can either be achieved with a scene or a source similar to [hiding your map](#Hide-your-map)
  
  You will want to set this up with a hot key that just switches to this scene/shows the source. Use this key before doing any of the activities that share information. Do not make it either a toggle or hold. Have a separate awkward hot key (Probably best with some meta keys such as Ctrl and Alt) to change it back/hide or change it manually. This is to stop accidentally showing the game undoing your hard work.
  
*  If you have rebound the console without clear to another key, make this trigger the game hide as well.
*  The report system shows Steam Profile names and Steam IDs. So I suggest making F7 trigger this scene/source as well.
*  Before entering the drone menu make sure you trigger the scene as it will show your map.
*  Harvesting bodies, as skulls show real profile names.
 
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
