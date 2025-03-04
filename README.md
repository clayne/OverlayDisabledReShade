# Overlay Disabled ReShade
Here's how to disable the ReShade Startup Message / Splash Screen on (almost) any version.  
DISCLAIMER: This modification is only recommended for advanced users. Proceed at your own risk.  
   
If you decide to use this build for a preset, remember to exclusively credit [***crosire***](https://github.com/crosire) and [***ReShade***](https://reshade.me)

## V4
### Link for [4.9.1 Release](https://github.com/FaridZelli/OverlayDisabledReShade/raw/main/ReShade_Setup_OverlayDisabled_491.exe)
- Note that these builds are extremely unstable, and should only be used for completed presets
- Hotkeys must be disabled

## Future Releases
### 5.4.x / 5.5.x
- Will build after all the hotfixes are released, or ReShade 5 becomes more stable


## DIY Method:  
In order to do it yourself, you will need:
1) Git
2) Visual Studio Community with C++, MSVS17 v141 Build Tools, .NET and Python modules installed
3) Notepad++

Step one:  
Head over to the official ReShade repository and clone everything, including the submodules  
https://github.com/crosire/reshade  

- Example for version 4.9.1  
```
git clone --recurse-submodules https://github.com/crosire/reshade.git
cd reshade
git checkout 1dd52078131b18d633a03519b80a0a5041c7ae6d
git submodule update
```  

Step two:  
Go to the ```source``` folder and find ```runtime_gui.cpp```  

Step three:  
Open the file in Notepad++ and do a replace all  
Find what: ```show_splash = true```  
Replace with: ```show_splash = false```  
Save, check if it applied, close  

Step four:  
Follow the instructions at https://github.com/crosire/reshade#building to build the setup  
```
build [Release] (32bit)
build [Release] (64bit)
build [Release Setup] (64bit)
```

## FAQ:
- **Q:** Why haven't you forked the project?   
**A:** I'm too lazy to maintain an actual fork out of this   
  
- **Q:** My computer exploded   
**A:** That's on you man
