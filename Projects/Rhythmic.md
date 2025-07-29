# Rhythmic
A basic reimplementation / demo covering the gameplay flow and mechanics of Amplitude (2016) by Harmonix in the Unity Engine

Amplitude by Harmonix is a Playstation 3/4-exclusive music-driven rhythm game designed for game controllers.

The game plays on a highway or tunnel of tracks, with each track being a particular instrument within the song. The goal of the game is to build up and complete the song by hitting notes at the right time, pressing the top buttons on the controller (L1, R1, R2) and by switching tracks using the D-pad or analog sticks.

While Rhythmic is compatible with songs from Amplitude, no proprietary assets from Amplitude ship with the project. These files have to be provided and converted by the user using their legally owned copy of Amplitude.

### Development timeline
**2020 Q1:** Project started  
**2021 Q1:** Technically playable status  
**2021 Q2:** Playable technical demo with initial visual polish  
**2021 Q4:** Development paused   _<-- (screenshots below)_  
**2023-now:** Ongoing refactors + system structure re-used for other projects

### Details

Rhythmic has the ability to use the original Amplitude game's metadata files, along with manually converted songs, to play the original songs in Rhythmic.

A custom song format and editor was planned, but not finished for a playable demo.

![Rhythmic in fullscreen](https://github.com/xezrunner/xezrunner/blob/main/Projects/Assets/Rhythmic-fullscreen.png?raw=true)

![Rhythmic in editor](https://github.com/xezrunner/xezrunner/blob/main/Projects/Assets/Rhythmic-in-Unity-Editor.png?raw=true)

### Systems

As part of this project, some in-game systems were created to help make prototyping and debugging easier. These systems got refactored and reused in future projects.

##### Debug menu and stats

Debug menu pages and menu item entries can be created and registered with a few lines of code. Variables, such as booleans and numbers, are automatically handled and can be adjusted through a keyboard or gamepad.

In later projects, functions that build menus can be marked with an attribute, which get dynamically registered automatically on startup, making them easier to create and use.

![Rhythmic's debug menu and stats display](https://github.com/xezrunner/xezrunner/blob/main/Projects/Assets/Rhythmic-debugmenu-and-stats.png?raw=true)

##### Debug console

A slide-down Quake-style debug console was created to facilitate console commands that can be invoked during gameplay.

Newest version of the console queries and registers commands dynamically during runtime by finding C# functions, variables and properties marked for console use.

Just like with the debug menu, the console also has support for recognizing basic types, like enums and numbers.

![Rhythmic's original debug console](https://github.com/xezrunner/xezrunner/blob/main/Projects/Assets/Rhythmic-debugconsole-pre.png?raw=true)

![XZShared debug console command example](https://github.com/xezrunner/xezrunner/blob/main/Projects/Assets/XZShared-debugconsole-command-example.png?raw=true)

![Rhythmic's in-development console](https://github.com/xezrunner/xezrunner/blob/main/Projects/Assets/Rhythmic-new-debugconsole.png?raw=true)