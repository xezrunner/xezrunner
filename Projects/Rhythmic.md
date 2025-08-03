# Rhythmic

A technical demo re-creating the gameplay flow and mechanics of Amplitude (2016) by Harmonix in the Unity game engine.

Amplitude by Harmonix is a Playstation 3/4-exclusive music-driven rhythm game designed for game controllers.

<div style="display: flex; gap: 5px; align-items: center; margin-bottom: 12px;">
  <!-- YouTube link -->
  <!-- TODO: record demo video
  <a href="https://youtu.be/PLACEHOLDER">
  <picture>
    <source media="(prefers-color-scheme: light)" srcset="https://github.com/xezrunner/xezrunner/blob/main/Projects/Assets/YT-light.png?raw=true">
    <source media="(prefers-color-scheme: dark)"  srcset="https://github.com/xezrunner/xezrunner/blob/main/Projects/Assets/YT-dark.png?raw=true">
    <img alt="YouTube link"
         src="https://github.com/xezrunner/xezrunner/blob/main/Projects/Assets/YT-light.png?raw=true"
         style="height: 52px;">
  </picture>
  </a>
  -->

  <!-- GitHub link -->
  <a href="https://github.com/xezrunner/Rhythmic">
  <picture>
    <source media="(prefers-color-scheme: light)" srcset="https://github.com/xezrunner/xezrunner/blob/main/Projects/Assets/GitHub-light.png?raw=true">
    <source media="(prefers-color-scheme: dark)"  srcset="https://github.com/xezrunner/xezrunner/blob/main/Projects/Assets/GitHub-dark.png?raw=true">
    <img alt="GitHub link"
         src="https://github.com/xezrunner/xezrunner/blob/main/Projects/Assets/GitHub-light.png?raw=true"
         style="height: 52px;">
  </picture>
  </a>
</div>

### About the game

Amplitude plays on a highway or tunnel of tracks, with each track being a particular instrument within the song. The goal of the game is to build up and complete the song by hitting notes at the right time, pressing the top buttons on the controller (L1, R1, R2) and by switching tracks using the D-pad or analog sticks.

While Rhythmic is compatible with songs from Amplitude, no proprietary assets from Amplitude ship with the project. These files have to be provided and converted by the user using their legally owned copy of Amplitude.

As it is a technical demo, the project is not intended to launch on storefronts, nor will the user experience completely substitute that of the original title's.

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

![Rhythmic's in-development console](https://github.com/xezrunner/xezrunner/blob/main/Projects/Assets/Rhythmic-new-debugconsole.png?raw=true)

![XZShared debug console command example](https://github.com/xezrunner/xezrunner/blob/main/Projects/Assets/XZShared-debugconsole-command-example.png?raw=true)