# Introduction
Hello, Charlemagne here. This is a guide on how to setup Velocity Plus for <a href = https://www.unrealengine.com/en-US>Unreal Engine</a>.
It's been a while since I first started my Sonic fangame journey, and because I didn't even know how to code at the time, I had to learn a lot by trials and errors. I actually started with <a href = https://github.com/GalaxySoftwareStudio/DashEngine>Dash Engine</a>, but switched to InfinityPlus, former version of V+.

Now, I want to help other people using Velocity Plus as it is an AMAZING framework for newcomers and veterans of the Sonic fangame community, with its fair share of simplicity and large amount of features and customizability.
Yet, Velocity Plus is not too easy to setup for people who are new to coding and game dev in general, and I know how it feels to be stuck on *rebuild from source manually* for hours.
In this guide, I'll help you setup the framework for UE4.27 and also give a few tips for those who wants V+ on UE5.

Quick disclaimer : I'm french, and some apps are set to french, but you can still find your way with the pictures attached.
# Table of content
- [[#0 - Prerequisites]]
- [[#1 - Visual Studio]]
  - [[#1.1 - Downloading Visual Studio 2022]]
  - [[#1.2 - Getting the proper options]]
- [[#2 - Setting up VelocityPlus]]
  - [[#2.1 - Disabling unused plugins]]
  - [[#2.2 - Visual Studio project files]]
  - [[#2.3 - Building InfinityPlus]]
- [[#3 - Launching VelocityPlus]]
# 0 - Prerequisites
- A generous amount of storage for Unreal Engine, VelocityPlus and possibly back ups.
- A decent computer. Check <a href = https://dev.epicgames.com/documentation/en-us/unreal-engine/hardware-and-software-specifications?application_version=4.27>UE4.27's recommended specs</a> and <a href = https://dev.epicgames.com/documentation/en-us/unreal-engine/hardware-and-software-specifications-for-unreal-engine>UE5's recommended specs</a> before starting.
- Being able to use a mouse and a keyboard.
- Visual Studio 2022 (2019 or 2017 can work with UE4.27 and 5, but 2022 is the latest version available so use it)
- UE4.27 (I personally recommend using UE4.27 for VelocityPlus if you're new to Unreal Engine, but it is possible to upgrade it to the newest versions of the engine (UE5.x). However, extra steps are needed for it to launch, and you'll have to fix a bunch of errors if you're converting an already modified version of V+. I recommend checking <a href = https://drive.google.com/drive/folders/1N9e2Mlbg6m1pARQ_Yi7mWCvN1TdNpmhM>Andy Miira's custom UE5 builds of V+</a> if you're starting a new project)
# 1 - Visual Studio
To begin setting up VelocityPlus, you'll need to get your hands on the latest version of Visual Studio since it is required to build the project.
You can also ignore this part and follow <a href = https://dev.epicgames.com/documentation/en-us/unreal-engine/setting-up-visual-studio-for-unreal-engine?application_version=4.27>UE's official guide on how to setup Visual Studio</a> as it is more detailed than mine.
## 1.1 - Downloading Visual Studio 2022

Download <a href=https://visualstudio.microsoft.com/vs>Visual Studio 2022</a> and run the setup executable. Once launched, you will need to install the 2022 community version ( you can use 2019 but 2022 is better if you consider doing other projects with UE5 as well ).

![[Pasted image 20250225175012.png]]
## 1.2 - Getting the proper options

For Visual Studio to work with Unreal Engine, you'll need to select the following options :
- Game development with C++ (under workloads)
- C++ profiling tools
- C++ AddressSanitizer (not required)
- Windows 10 SDK (10.0.18362.0 or newer)
- Unreal Engine installer

![[Pasted image 20250225175407.png]]
After selecting those, you can proceed with the installation.
# 2 - Setting up VelocityPlus
Now that we've got VS installed, we'll be able to set up VelocityPlus properly. Download <a href = https://drive.google.com/drive/folders/1mFyQVtEOp_JPwU87O49GzNMc2SFuIEYB?usp=sharing>V+'s project files</a> ( and not the demo ) and extract it on your computer. It's better to keep the zip file around if you ever mess something up and you need to get a quick backup.
## 2.1 - Disabling unused plugins
First, you'll want to disable plugins that you don't have from the .uproject file. To do so, right click on VelocityPlus.uproject and open with NotePad.

![[Pasted image 20250225180721.png]]
*Note : if you don't see UE's blue logo on the .uproject file, go to \Epic Games\Launcher\Engine\Binaries\Win64 and launch UnrealVersionSelector.exe!*

Inside NotePad, disable plugins that you don't have by setting "true" to "false" after "enabled".
![[Pasted image 20250225181521.png]]
Save and exit NotePad once you're done.
## 2.2 - Visual Studio project files
Now that unused plugins are out of the way, right click VelocityPlus.uproject and select "Generate Visual Studio project files".
![[Pasted image 20250225181730.png]]

Select UE4.27, and proceed with the generation. Once finished, you should have new folders, and a new file.
![[Pasted image 20250225182119.png]]
Double click VelocityPlus.sln. Visual Studio will open.
# 2.3 - Building InfinityPlus
In order to launch VelocityPlus, you'll need to build the solution first. After opening VelocityPlus.sln, you will be met with Visual Studio's interface.
![[Pasted image 20250225182456.png]]

Find the solution explorer on the left, and right click on VelocityPlus. Then, select "Generate". The bottom window will give you info on the current state of the generation.
![[Pasted image 20250225182833.png]]
![[Pasted image 20250225183007.png]]
Once finished, make sure the build was successful. Check if the final message shows one success and zero failure.
![[Pasted image 20250225183530.png]]
# 3 - Launching VelocityPlus
Finally, you can exit Visual Studio and double click VelocityPlus.uproject. Wait for it to start, and if everything was done properly, you should be met with this loading screen.
![[Pasted image 20250225183753.png]]

Now, the project may or may not take a large amount of time compiling shaders depending on your PC's specs. Let it do its things and the project should open properly.
Once everything is ready, you should find yourself in L_DebugRoomMas, and you can start doing whatever you want with the framework.

![[Pasted image 20250225190107.png]]