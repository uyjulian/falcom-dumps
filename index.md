---
layout: default
title: Falcom 3D texture and model dumps
---

# Introduction

This page contains Falcom 3D model and texture dumps.

# Recommended downstream resources

The following people have used the model dumps on this page to create derivative works.  
If you have questions about usage of the models in a specific environment, sending messages to people with experience in the specific environment may be a good idea.  

## VRChat

### PMONickpop123
* [Trista](https://vrchat.com/home/launch?worldId=wrld_2734091a-fd00-4fbc-9ca4-12cd8298793f)  
* [Hamel](https://vrchat.com/home/launch?worldId=wrld_482b2940-d8e5-482a-b63b-00e876d371cc)  
* [Celdic](https://vrchat.com/home/launch?worldId=wrld_66ffde02-15d5-499c-9bbb-c518b7a6beae)  
* [Celestial Globe](https://vrchat.com/home/launch?worldId=wrld_3ef10b33-084f-49f0-9fb4-6a328ff09213)  
* [The Infernal Castle](https://vrchat.com/home/launch?worldId=wrld_a086cc54-958e-496c-a0ab-b247eece1e9c)  
* [Garrelia Fortress](https://vrchat.com/home/launch?worldId=wrld_21ab4751-42b2-4cb1-b191-20dbb8f251ed)  

### Nerzarn
* [Courageous](https://vrchat.com/home/launch?worldId=wrld_1e0e204d-1145-4df9-8560-6d92c4fbffe3)  
* [Lohengrin Castle](https://vrchat.com/home/launch?worldId=wrld_615beb64-4820-411c-85b5-d1dedbfcbb7f)  
* [Trails avatars](https://vrchat.com/home/launch?worldId=wrld_f309b11e-8ca1-42ac-b518-ec149eeed9dd)  
* [Alster](https://vrchat.com/home/launch?worldId=wrld_107ffde2-8e67-48fd-9cf7-c1a5a646912d)  

### Kressik
* [Orchis Tower - Trails Avatars](https://vrchat.com/home/launch?worldId=wrld_74731336-347f-43f1-b861-26fa0acf7124)  
* [Orchis Tower - Trails Avatars](https://vrchat.com/home/launch?worldId=wrld_de7035d7-eaa0-4a68-ac44-285c0e9303fb)  

### Seedoo
* [Ymir](https://vrchat.com/home/launch?worldId=wrld_87b1558f-66d4-403c-a76d-0f2c3d66fe1c)  
* [Lake Lacrima](https://vrchat.com/home/launch?worldId=wrld_fcadb7b9-002b-4258-97fa-31f637abd16e)  
* [Heimdallr](https://vrchat.com/home/launch?worldId=wrld_879fedbb-fb12-4341-b122-9c6ef4508da2)  

### RiasVonGremory
* [Eryn](https://vrchat.com/home/launch?worldId=wrld_0e6f06fc-c6d3-40e8-a8ce-42093d4af1c2)  

### Hai no Kishin
* [Phantasma](https://vrchat.com/home/launch?worldId=wrld_7473e962-5c57-4343-8eb4-e1a3f3bf18d0)  

### FireyKitsune
* [Leeves](https://vrchat.com/home/launch?worldId=wrld_89d6105e-d01b-426f-b253-b762b2b3f45a)  
* [Radio Trista in Leeves](https://vrchat.com/home/launch?worldId=wrld_3c58a9d0-1e4f-4f88-8880-adc6cfec324d)  

## NeosVR

### uyjulian
Sen1+2 avatars: `neosrec:///U-uyjulian/R-fb409dac-4f4d-4b46-9517-917866f508e9`  

# Questions and answers

## How do I use the models?
You can use the GLTF/GLB import functionality of your 3D program. If you are not sure about how to access this functionality, I suggest that you gain more experience with your 3D program.  

## How do I convert GLTF/GLB to FBX and PNG files?
You can use the GLTF/GLB import functionality and the FBX export functionality of [Blender](https://www.blender.org/), which is a free 3D program.  

To ensure that the PNG files are also output in the same directory as the FBX file, make sure the "Path Mode" is set to "Copy" in the FBX export settings.  

An alternative to using Blender to convert GLTF files to FBX is to use [Noesis](https://www.richwhitehouse.com/index.php?content=inc_projects.php&showproject=91).  
However, I recommend that you try using Blender to convert files before using Noesis.  

## After exporting to FBX, why does one half of the model file have wrongly mapped textures?
In the program, you need to set the texture repeat mode to "Repeat".  

In Unity, this can be done from the texture inspector window.  
Please see the [Unity documentation on TextureImporter](https://docs.unity3d.com/Manual/class-TextureImporter.html) for a visual of the texture inspector window.  

## What format are the PNG textures in?
They are in the smallest uncompressed format, in order to get more gains when inside a solid 7-zip archive.  

## How do I get the high resolution face textures for Sen3, Sen4, and Hajimari?
For high resolution face textures, please use the file `fc_chrXXXfYY_conv` instead of `chrXXX_YY_conv`.  

## How do I apply animations to models in Blender?

To apply animations:  
1. Import both model and animation with "Bone Dir" set to "Blender" (otherwise it may look wrong)  
2. Open "Dope Sheet" (shift-F12)  
3. On the drop down box saying "Dope Sheet" click on "Action Editor"  
4. In the "Outliner" window click on the model  
5. To the left where it says "New" click is a drop down box  
6. Select the animation  

Now the animation should be applied.  
It may be possible that the keyframes may be e.g. 100 seconds away.  
To see where the keyframes are, disable "Only Show Selected" (the arrow icon) in the "Dope Sheet" view of Blender, then scroll to the right.  

For some models, the animation data may not be offset from the first keyframe instead of the initial position of the bone.  
In this case, please use [this](https://gist.github.com/uyjulian/526c8c7326b0bd7031875c5973144000) script to "bake" the bone positions so that it is offset from the first keyframe.  

## The archive is very large. How can I extract individual files?
You can extract individual texture files using the 7-Zip GUI.  
Alternatively, you can use the 7-zip command line:  
```bat
7z x -r -o. texture_archive.7z file1.dds file2.dds ...
```
To figure out which files to extract, attempt to import the model file into a 3D modeling program, then look at the list of missing textures.  

## Do the models and/or textures contain spoilers for that specific game?
Yes, they contain spoilers for that respective game. If you have not played that specific game and do not want to get spoiled, do not open the model or texture files in your viewer.  

## Are models for the DLC outfits included?
For Sen1 and Sen2, they are included thanks to them being included in the update files.  
For Sen3 and Sen4, and Hajimari, the files that are included with the PC version of the game are included.  

## I reached the MEGA bandwidth limit. What are my options?
MEGA has a premium service. You can subscribe to the cheapest plan and complete the download.  
Alternatively, if you have multiple connections with a unique IP (example: mobile connection or VPN), you can switch between them.  
After that is done, refresh the page then continue the download.  

## The map models appear to be missing geometry. Where can I get the geometry?  
The object and plant transformations are stored in a separate `.ops` and `.plt` files, respectively.  
The program "[EDOpsParser](https://github.com/uyjulian/EDOpsParser)" can print information about these files.  
Please contact me for more information about these files.  

## How do I extract the .pkg data from the PSARC file?
For PS3 and PSVita, please visit the [PS3 Dev Wiki page on PSARC](https://www.psdevwiki.com/ps3/PlayStation_archive_(PSARC)).  
For PS4, you will need to use the `orbis-psarc` tool. This utility can be found easily using a search engine.  

## How do I extract the .pkg data from the BRA file?
The following program can be used for this purpose: [Heroes of Legend forum topic](https://heroesoflegend.org/forums/viewtopic.php?t=356)  

## How do I extract the .pkg data from the PKA file?
The [unpackpka](https://github.com/uyjulian/unpackpka) program can be used for this purpose.  

## How do I extract the files from the .pkg file?
The following [QuickBMS](http://aluigi.altervista.org/quickbms.htm) script can be used for this purpose: [Link to QuickBMS script](http://aluigi.altervista.org/bms/legend_of_heroes.bms)  

A [Python script](https://gist.github.com/uyjulian/55475c98c631632ddfd5453469726439) is also available for .pkg extraction.  

## How do I get the texture data out of the PhyreEngine cluster format?
If you have file names ending in `.phyre`, such as `.bmp.phyre`, `.png.phyre`, `.dds.phyre`, some certain utilities are used to retrieve the texture data.

The following [Noesis](https://richwhitehouse.com/index.php?content=inc_projects.php&showproject=91) script can be used for this purpose: [ZenHAX forum topic](https://zenhax.com/viewtopic.php?f=7&t=7573)  

## How do I get the model data out of the .pkg file?
The [ed8pkg2glb](https://github.com/uyjulian/ed8pkg2glb) program can be used for this purpose.  

## How do I get the model data out of the PhyreEngine cluster format?
If you retrieved the `.dae.phyre` file out of the .pkg file, please see the above section.  

# Model and texture dumps

## Trails in the Sky / Sora no Kiseki / Zero no Kiseki / Ao no Kiseki
See [Ribose's Trails asset dumps](https://mega.nz/#F!OsF2Ub5S!xvaFj8Zy1J5iO1aYT-xKlA).  
For Sora PC 3D model viewing, see [OpenSora](https://github.com/rds1983/OpenSora).  
For Zero/Ao PSP 3D model extraction, see [it3cnv](https://www.pokanchan.jp/dokuwiki/software/itxcnv#it3_converter).  

## Trails of Cold Steel / Sen no Kiseki / Hajimari no Kiseki

Sen1+2 Character models, textures, and animations (GLB/GLTF binary combined format): [MEGA](https://mega.nz/file/psJHBAiT#GZ7RrqN_VewHKRI7ZIDsxU34XnOLMOZxUzM6msSEwog)  

Sen3+4+Hajimari Character models, textures, and animations (GLB/GLTF binary combined format): [MEGA](https://mega.nz/file/xhBxlCqJ#TEE4Q3NsrWC98WJ35AYzdm4YnhqRPCpIPybrHFvr5MM)  

Due to size considerations, I am no longer providing non-character textures or models publically. These files can be extracted from the PC version of the game.  

## Kuro no Kiseki

Dumped with 9.00 exploit.  
WIP 3D model extracted: [MEGA](https://mega.nz/file/gsJ1HSpK#l8DLSA1e2cau0UGdlK83hMwNiwTBguBmHFWM77zMZz8)  
Currently skins, textures, and animations are missing.  

## Other Falcom games

Due to size considerations, I am no longer providing textures or models publically. These files can be extracted from the PC version of the game.  

[Go to the top of the page](#)  
[Return to top page](..)  
