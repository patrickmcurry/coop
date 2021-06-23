Millennium Co-Op for Quake 1
by Patrick Curry http://patrickcurry.com/
Originally finished Dec 17, 2016

*** About this Mod: ***

My goal with Millennium Co-Op is to tune and tweak Quake 1 for a slightly more enjoyable cooperative play experience.
I'm not trying to change the game: there aren't new levels, weapons, powerups, or monsters.  Instead, I just want
to make the game more fun to play with friends.  This mod should be playable on all maps created for vanilla
Quake 1.

*** Changes from basic Quake co-op rules: ***

* You slowly regenerate health back up to 25, but only after a few seconds of not taking damage or attacking
* After you die you have to wait a few seconds before coming back into the game... the more you die... the longer you wait
* If teamplay is on, then no players can harm each other (instead of just players of the same color)
   * this is done via "teamplay 1" at the console
* Only one player can carry a key at a time...
   * When you die while carrying the key, it will drop at your feet
   * If no one collects it in 30 seconds, the key returns to it's initial spawn point
* Only one player can pickup each weapon...
   * When you die, all of your guns go into your pack
   * You respawn with only the shotgun... so you have to go after your pack
   * If no one collects your pack after two minutes, the guns respawn at their initial points
   * If you had a gun in your pack that isn't placed in the current level, it's gone
* Ability to set a maximum number of respawns to keep the game intense
   * Works for each individual player or a total respawn count for all player
   * The default is infinite respanws: "saved1 0"
   * Use "saved1 3" to give each player 3 respawns
   * Just add 1000 to the number to make it a team-wide value: "saved1 1003"
   * Use -1 to mean no respawning at all: "saved1 -1"
* Most player actions are broadcast to all players:
   * Picking up a weapon, key, armor, or powerup
   * Finding a secret
* Special bonuses for killing all monsters and finding all secrets
   * You'll have to play to find out what!

*** Installation: ***

Copy progs.dat into a new "coop" folder in your Quake directory.  Only the computer hosting the game needs the mod.  
All players can connect to the server without new files being installed.

*** Running a Server: ***

The simple version: run this from the command line in your quake directory...

winquake -game coop

And then use the main menu to start a coop server.  I use the following command to start up a non-dedicated Millennium Co-Op server...

winquake -game coop -winmem 64 -listen 8 +coop 1 +map start

You can replace "winquake" with any Quake client that supports original mods.  The only other app I've tried it with is
GLQuake.exe.  Set the value after "-listen" to be the number of clients you want to support.
