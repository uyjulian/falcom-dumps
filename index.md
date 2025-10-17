---
layout: default
title: Falcom 3D texture and model dumps
---

# Introduction

This page contains Falcom 3D model and texture dumps.

# Modding resources

For resources relating to modding Trails/Kiseki games (including a **Discord** server), see [Trails Research Group](https://github.com/Trails-Research-Group).  

# Recommended downstream resources

The following people have used the model dumps on this page to create derivative works.  
If you have questions about usage of the models in a specific environment, sending messages to people with experience in the specific environment may be a good idea.  

## VRChat

See [Trails into VR](https://trails-into-vr.github.io/) for a list of VRChat content.

## Resonite

### uyjulian
Public folder: `resrec:///U-uyjulian/R-fb409dac-4f4d-4b46-9517-917866f508e9`  

# Questions and answers

### How do I use the models?
You can use the GLTF/GLB import functionality of your 3D program. If you are not sure about how to access this functionality, I suggest that you gain more experience with your 3D program.  

### How do I convert GLTF/GLB to FBX and PNG files?
You can use the GLTF/GLB import functionality and the FBX export functionality of [Blender](https://www.blender.org/), which is a free 3D program.  

To ensure that the PNG files are also output in the same directory as the FBX file, make sure the "Path Mode" is set to "Copy" in the FBX export settings.  

An alternative to using Blender to convert GLTF files to FBX is to use [Noesis](https://www.richwhitehouse.com/index.php?content=inc_projects.php&showproject=91).  
However, I recommend that you try using Blender to convert files before using Noesis.  

### How do I extract PNG texture files from the GLB file?
You can use the GLTF/GLB import functionality of [Blender](https://www.blender.org/), which is a free 3D program.  

In Blender, select the following menu option: File->External->Unpack Resources  

### After exporting to FBX, why does one half of the model file have wrongly mapped textures?
In the program where the FBX file is being imported, you need to set the texture repeat mode to either "Repeat" or "Mirror". Use visual feature detection to determine the correct mode to set.  

In Unity, this can be done from the texture inspector window.  
Please see the [Unity documentation on TextureImporter](https://docs.unity3d.com/Manual/class-TextureImporter.html) for a visual of the texture inspector window.  

### What format are the PNG textures in?
They are in the smallest uncompressed format, in order to get more gains when inside a solid 7-zip archive.  

### How do I get the high resolution face textures for Sen3, Sen4, and Hajimari?
(!!!: High resolution face textures are not included in the current dump. This will be fixed in the future.)  
For high resolution face textures, please use the file `fc_chrXXXfYY_conv` instead of `chrXXX_YY_conv`.  

### How do I apply animations to models in Blender?
(!!!: Animations in the dump may be broken, even after using these steps. This will be fixed in the future.)  

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

### The archive is very large. How can I extract individual files?
You can extract individual texture files using the 7-Zip GUI.  
Alternatively, you can use the 7-zip command line:  
```bat
7z x -r -o. texture_archive.7z file1.dds file2.dds ...
```
To figure out which files to extract, attempt to import the model file into a 3D modeling program, then look at the list of missing textures.  

### Do the models and/or textures contain spoilers for that specific game?
Yes, they contain spoilers for that respective game. If you have not played that specific game and do not want to get spoiled, do not open the model or texture files in your viewer.  

### Are models for the DLC outfits included?
For Sen1 and Sen2, they are included thanks to them being included in the update files.  
For Sen3 and Sen4, and Hajimari, the files that are included with the PC version of the game are included.  

### I reached the MEGA bandwidth limit. What are my options?
MEGA has a premium service. You can subscribe to the cheapest plan and complete the download.  
Alternatively, if you have multiple connections with a unique IP (example: mobile connection or VPN), you can switch between them.  
After that is done, refresh the page then continue the download.  

### The map models appear to be missing geometry. Where can I get the geometry?  
The object and plant transformations are stored in a separate `.ops` and `.plt` files, respectively.  
The program "[EDOpsParser](https://github.com/uyjulian/EDOpsParser)" can print information about these files.  
Please contact me for more information about these files.  

### How do I extract the .pkg data from the PSARC file?
For PS3 and PSVita, please visit the [PS3 Dev Wiki page on PSARC](https://www.psdevwiki.com/ps3/PlayStation_archive_(PSARC)).  
For PS4, you will need to use the `orbis-psarc` tool. This utility can be found easily using a search engine.  

### How do I extract the .pkg data from the BRA file?
The following program can be used for this purpose: [Heroes of Legend forum topic](https://heroesoflegend.org/forums/viewtopic.php?t=356)  

### How do I extract the .pkg data from the PKA file?
The [unpackpka](https://github.com/uyjulian/unpackpka) program can be used for this purpose.  

### How do I extract the files from the .pkg file?
The following [QuickBMS](http://aluigi.altervista.org/quickbms.htm) script can be used for this purpose: [Link to QuickBMS script](http://aluigi.altervista.org/bms/legend_of_heroes.bms)  

The [unpackpkg](https://github.com/uyjulian/unpackpkg) program is also available for `.pkg` extraction.  

### How do I get the texture data out of the PhyreEngine cluster format?
If you have file names ending in `.phyre`, such as `.bmp.phyre`, `.png.phyre`, `.dds.phyre`, some certain utilities are used to retrieve the texture data.

The following [Noesis](https://richwhitehouse.com/index.php?content=inc_projects.php&showproject=91) script can be used for this purpose: [ZenHAX forum topic](https://zenhax.com/viewtopic.php?f=7&t=7573)  

### How do I get the model data out of the .pkg file?
The [ed8pkg2glb](https://github.com/uyjulian/ed8pkg2glb) program can be used for this purpose.  

### How do I get the model data out of the PhyreEngine cluster format?
If you retrieved the `.dae.phyre` file out of the .pkg file, please see the above section.  

# Model and texture dumps

### Trails in the Sky / Sora no Kiseki / Zero no Kiseki / Ao no Kiseki
See [Ribose's Trails asset dumps](https://mega.nz/#F!OsF2Ub5S!xvaFj8Zy1J5iO1aYT-xKlA).  
For Sora PC 3D model viewing, see [OpenSora](https://github.com/rds1983/OpenSora).  
For Zero/Ao PSP 3D model extraction, see [it3cnv](https://www.pokanchan.jp/dokuwiki/software/itxcnv#it3_converter).  

### Trails of Cold Steel / Sen no Kiseki / Hajimari no Kiseki

Due to size considerations, I am no longer providing assets from these games publically. These files can be extracted from the PC version of the game using the `ed8pkg2glb` tool mentioned above.  

### Trails through Daybreak / Kuro no Kiseki

Kuro Character models (GLTF model+animation data only) (v4): [MEGA](https://mega.nz/file/RwA0hDzY#mSD4BLlIb6uzvqbXwZrkp7vYoJmp09sxJk4e9nGxe3w)  
Kuro Character model textures (PNG texture data only) (v2): [MEGA](https://mega.nz/file/Ql4iWKJK#rw30oUG-iaZIzhTotV48YSPED1sRR9FcLyGz06xetKA)  
Kuro Equipment models (GLTF model+animation data only) (v4): [MEGA](https://mega.nz/file/1oYmAL5S#tApAAS00pZEqyYk8-gsc1iG8H6eh_lXffI7e3aFceAg)  
Kuro Equipment model textures (PNG texture data only) (v2): [MEGA](https://mega.nz/file/thB3DbYQ#u9XvNwPcc1wWWscizy-Kw9v6Hl64_4xNdfUbNXh1GXc)  

Due to size considerations, I am no longer providing non-character textures or models publically.  

### Trails through Daybreak 2 / Kuro no Kiseki 2

Kuro 2 Character models (GLTF model+animation data only) (v4): [MEGA](https://mega.nz/file/4pRFjSQK#9rnqnwOig2I3sfDuZwMfj1zGTFuDI0z7M4m16ltSSS0)  
Kuro 2 Character model textures (PNG texture data only) (v2): [MEGA](https://mega.nz/file/E05jiIhZ#XVdWqhMOsaWUiyUqGY0yi-9cZnsc8yMO55ExQQtrSyM)  
Kuro 2 Equipment models (GLTF model+animation data only) (v4): [MEGA](https://mega.nz/file/J8IBkSrB#DS86qMuBQgdIebDHa4BAW5xFca5i7cRMza5aPu9h0bY)  
Kuro 2 Equipment model textures (PNG texture data only) (v2): [MEGA](https://mega.nz/file/JsQUhC5T#-22SmJHUT12puCF3wtrM8K0ffdyOliUM-STY7W3dFOA)  

Due to size considerations, I am no longer providing non-character textures or models publically.  

### Kai no Kiseki

Kai Character models (GLTF model+animation data only) (v4.1): [MEGA](https://mega.nz/file/NtwllaoS#kJRZmCgq_-XRj9CkOFyl9_o4phnG8wn6SXD4XzE6-yc)  
Kai Character model textures (PNG texture data only) (v2): [MEGA](https://mega.nz/file/IwR0wBJY#aksNqVf-98rlJnNO_n87-mVbpPE91xkARiIHdOi2uQg)  
Kai Equipment models (GLTF model+animation data only) (v4.1): [MEGA](https://mega.nz/file/U851lKxb#vGrLw9Q2Cy0BS9NAKXtE84-CqnE8t6lAyd7LJv8Z8aQ)  
Kai Equipment model textures (PNG texture data only) (v2): [MEGA](https://mega.nz/file/phwz0I4C#hYzVbAjc4hj8NyvCRzC6GcbOlKZEBRsUr7D04TbcXSU)  

Due to size considerations, I am no longer providing non-character textures or models publically.  

### Sora no Kiseki / Trails in the Sky (remake)

Sora 1st Character models (GLTF model+animation data only) (v4.1): [MEGA](https://mega.nz/file/YhBgFbwR#GnOfOZl3MS4cScsg7xDIY6PimuOT6JYYBweUBwIbMTM)  
Sora 1st Character model textures (PNG texture data only) (v2): [MEGA](https://mega.nz/file/9xQx1K5J#b7S_kQKTpPUN8EBzh9a0MJFfZdHfEnwayJZiZnSOpXY)  
Sora 1st Equipment models (GLTF model+animation data only) (v4.1): [MEGA](https://mega.nz/file/kxQBVZjJ#zgsw5hI0qBpwCjJ2q2IKhFgCYGrwzf4HutalqD1XIaQ)  
Sora 1st Equipment model textures (PNG texture data only) (v2): [MEGA](https://mega.nz/file/tpglCDZD#wv4XheB-acZdaNJdSPgIGrAdOoFImAA1IyFh7l2RxI0)  

Due to size considerations, I am no longer providing non-character textures or models publically.  

### Other Falcom games

Due to size considerations, I am no longer providing assets from these games publically. These files can be extracted from the PC version of the game using the tools mentioned above.  

[Go to the top of the page](#)  
[Return to top page](..)  
