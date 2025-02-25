# Introduction
Hello, Charlemagne here. This is a guide on how to setup Velocity Plus for <a href="https://www.unrealengine.com/en-US">Unreal Engine</a>.
It's been a while since I first started my Sonic fangame journey, and because I didn't even know how to code at the time, I had to learn a lot by trials and errors. I actually started with <a href="https://github.com/GalaxySoftwareStudio/DashEngine">Dash Engine</a>, but switched to InfinityPlus, former version of V+.

Now, I want to help other people using Velocity Plus as it is an AMAZING framework for newcomers and veterans of the Sonic fangame community, with its fair share of simplicity and large amount of features and customizability.
Yet, Velocity Plus is not too easy to setup for people who are new to coding and game dev in general, and I know how it feels to be stuck on *rebuild from source manually* for hours.
In this guide, I'll help you setup the framework for UE4.27 and also give a few tips for those who wants V+ on UE5.

Quick disclaimer : I'm french, and some apps are set to french, but you can still find your way with the pictures attached.
# Table of content
- 0 - Prerequisites
- 1 - Visual Studio
  - 1.1 - Downloading Visual Studio 2022
  - 1.2 - Getting the proper options
- 2 - Setting up VelocityPlus
  - 2.1 - Disabling unused plugins
  - 2.2 - Visual Studio project files
  - 2.3 - Building InfinityPlus
- 3 - Launching VelocityPlus
# 0 - Prerequisites
- A generous amount of storage for Unreal Engine, VelocityPlus and possibly back ups.
- A decent computer. Check <a href="https://dev.epicgames.com/documentation/en-us/unreal-engine/hardware-and-software-specifications?application_version=4.27">UE4.27's recommended specs</a> and <a href = "https://dev.epicgames.com/documentation/en-us/unreal-engine/hardware-and-software-specifications-for-unreal-engine">UE5's recommended specs</a> before starting.
- Being able to use a mouse and a keyboard.
- Visual Studio 2022 (2019 or 2017 can work with UE4.27 and 5, but 2022 is the latest version available so use it)
- UE4.27 (I personally recommend using UE4.27 for VelocityPlus if you're new to Unreal Engine, but it is possible to upgrade it to the newest versions of the engine (UE5.x). However, extra steps are needed for it to launch, and you'll have to fix a bunch of errors if you're converting an already modified version of V+. I recommend checking <a href = "https://drive.google.com/drive/folders/1N9e2Mlbg6m1pARQ_Yi7mWCvN1TdNpmhM">Andy Miira's custom UE5 builds of V+</a> if you're starting a new project)
# 1 - Visual Studio
To begin setting up VelocityPlus, you'll need to get your hands on the latest version of Visual Studio since it is required to build the project.
You can also ignore this part and follow <a href="https://dev.epicgames.com/documentation/en-us/unreal-engine/setting-up-visual-studio-for-unreal-engine?application_version=4.27">UE's official guide on how to setup Visual Studio</a> as it is more detailed than mine.
## 1.1 - Downloading Visual Studio 2022

Download <a href="https://visualstudio.microsoft.com/vs">Visual Studio 2022</a> and run the setup executable. Once launched, you will need to install the 2022 community version ( you can use 2019 but 2022 is better if you consider doing other projects with UE5 as well ).

![image](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225175012.png?raw=true)
## 1.2 - Getting the proper options

For Visual Studio to work with Unreal Engine, you'll need to select the following options :
- Game development with C++ (under workloads)
- C++ profiling tools
- C++ AddressSanitizer (not required)
- Windows 10 SDK (10.0.18362.0 or newer)
- Unreal Engine installer

![image2](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225175407.png?raw=true)
After selecting those, you can proceed with the installation.
# 2 - Setting up VelocityPlus
Now that we've got VS installed, we'll be able to set up VelocityPlus properly. Download <a href="https://drive.google.com/drive/folders/1mFyQVtEOp_JPwU87O49GzNMc2SFuIEYB?usp=sharing">V+'s project files</a> ( and not the demo ) and extract it on your computer. It's better to keep the zip file around if you ever mess something up and you need to get a quick backup.
## 2.1 - Disabling unused plugins
First, you'll want to disable plugins that you don't have from the .uproject file. To do so, right click on VelocityPlus.uproject and open with NotePad.

![image3](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225180721.png?raw=true)
*Note : if you don't see UE's blue logo on the .uproject file, go to \Epic Games\Launcher\Engine\Binaries\Win64 and launch UnrealVersionSelector.exe!*

Inside NotePad, disable plugins that you don't have by setting "true" to "false" after "enabled".
![image4](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225181521.png?raw=true)
Save and exit NotePad once you're done.
## 2.2 - Visual Studio project files
Now that unused plugins are out of the way, right click VelocityPlus.uproject and select "Generate Visual Studio project files".
![image5](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225181730.png?raw=true)

Select UE4.27, and proceed with the generation. Once finished, you should have new folders, and a new file.
![image6](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225182119.png?raw=true)
Double click VelocityPlus.sln. Visual Studio will open.
# 2.3 - Building InfinityPlus
In order to launch VelocityPlus, you'll need to build the solution first. After opening VelocityPlus.sln, you will be met with Visual Studio's interface.
![image7](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225182456.png?raw=true)

Find the solution explorer on the left, and right click on VelocityPlus. Then, select "Generate". The bottom window will give you info on the current state of the generation.
![image8](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225182833.png?raw=true)
![image9](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225183007.png?raw=true)
Once finished, make sure the build was successful. Check if the final message shows one success and zero failure.
![image10](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225183530.png?raw=true)

Note : For those building the project for UE5, you might encounter this error message in the build :
![image11](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225204343.png?raw=true)
You'll need to do a few things for it to work.

First, go into \Config and open DefaultGame.ini with NotePad.
![image12](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225204629.png?raw=true)
Inside, select edit and replace ( or ctrl + H ). Then, input IniKeyBlacklist in research, and IniKeyDenylist in replace. Press "replace all", save and close.
![image13](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225204934.png?raw=true)
![image14](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225204944.png?raw=true)

Then, in Visual Studio, go into InfinityPlusEditor.Target.cs and InfinityPlus.Target.cs and replace 'DefaultBuildSettings = BuildSettingsVersion.V2;' with 'DefaultBuildSettings = BuildSettingsVersion.V5;'.
![image15](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225205542.png?raw=true)

After that, add 'IncludeOrderVersion = EngineIncludeOrderVersion.Unreal5_5;' and 'CppStandard = CppStandardVersion.Cpp20;' in InfinityPlusEditor.Target.cs
![image16](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225205918.png?raw=true)

Finally, disable NiagaraExtra or any unfound plugins in the .uproject file as it will prevent the build process to finish.
![image17](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225210240.png?raw=true)

Now, save and build VelocityPlus again. The build should be successful.
![image18](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225210729.png?raw=true)
(If you encounter errors that don't tell you exactly why they're happening, check in your Unreal Library if each plugin works with the latest version of the engine)
# 3 - Launching VelocityPlus
Finally, you can exit Visual Studio and double click VelocityPlus.uproject. Wait for it to start, and if everything was done properly, you should be met with this loading screen.
![image19](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225183753.png?raw=true)

Now, the project may or may not take a large amount of time compiling shaders depending on your PC's specs. Let it do its things and the project should open properly.
Once everything is ready, you should find yourself in L_DebugRoomMas, and you can start doing whatever you want with the framework.

On UE4:
![image20](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225190107.png?raw=true)
On UE5:
![image21](https://github.com/CharlemagneXXI/Images/blob/main/Pasted%20image%2020250225212922.png?raw=true)
# End
I hope this guide helped you to setup V+ properly on your PC. If you ever encounter issues that aren't covered here, you can let me know through V+'s discord server or on GitHub. I'll make sure to read them and find fixes whenever I can.
Have fun using VelocityPlus! Good luck with your projects!
