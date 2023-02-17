# MMGG
GGMM reverese engeering!

I think I'm not allowed to put original files here, but I can give you a link:

https://www.gtagarage.com/mods/show.php?id=434

and I will put my REVENGed files of GGMM, I call it MMGG project :3

I already mailed initial and original programmer and recieved no answers, metdata shows he's been offline for like 15 years! I hope he's still alive!
________________________________

Ok... It's my first time that I wana back engineer sth, never done it before!

Alright here we are, in a directory with following files:

```shell
┌──(user㉿dhcppc4)-[~/Desktop/books/MMGG]
└─$ ls
GGMM.exe  GGMM.txt  GTAINTERFACE.dll
    
```

I knwo that de pogram was created using Delfi lang, and I know nothing of Delfi, but I think it' safe ti stick into standard procedure, Which is scanning the file types:3

```shell
┌──(user㉿dhcppc4)-[~/Desktop/books/MMGG]
└─$ file * 
GGMM.exe:         PE32 executable (GUI) Intel 80386, for MS Windows, UPX compressed
GGMM.txt:         ASCII text, with very long lines (376), with CRLF line terminators
GTAINTERFACE.dll: PE32 executable (DLL) (GUI) Intel 80386, for MS Windows
     
```
Now what does it tell us?! A lot to go abviously :3

From all em files. I only know the structure of the .txt file which is `GGMM.txt` , You wanna see? simply just cat it!

```shell
┌──(user㉿dhcppc4)-[~/Desktop/books/MMGG]
└─$ cat GGMM.txt 
set word wrap to ON to read this file properly.

________________________________________________________________________________
this program should not be distributed anywhere else than www.gtatools.com or
other gtanet sites such as http://www.gtagarage.com. if you distribute this program
on any other website your server shall crash and burn in flames and your 
girlfriend will leave you next evening if you don't always update the program 
to latest version, please read the informations about distribution on 
www.gtatools.com.
________________________________________________________________________________
GTA Garage Mod Manager 2.3C build: 070207
This program is only for PC version of Grand Theft Auto games.

Copyright 2005-2007 Delfi - Jernej L. 
email: jernej@gtatools.com

always get latest and up-to-date copy of the program at http://www.gtatools.com or http://www.gtagarage.com

this program is a fully featured car packager / installer / renderer (3D) and helps creating custom cars.

program is freeware, you may NOT gain any money with using, redistributing, copying, changing this file unless you have my permission! 

the program comes with no warranty and the author is not responsible for anything the program or his user do under any circumstances, if this is against your local laws or you don't agree to this then you are not authorised to use the program.

________________________________________________________________________________

Installation
________________________________________________________________________________

extract the archive files into your gta installation directory (gta3, vice city or san andreas), this enables you to use the program with several games at once.

the ggmm.exe, gtainterface.dll and ggmm.txt should be IN exact same folder as gta3.exe, gta-vc.exe or gta_sa.exe

after you install it, click the help "?" button on program and set file association for .GGM files

important note !!
!!!!!!! only one program can control the file asociation at once !!!!!!!

program requirements:
- this program requires at least geforce3 class graphical card (but older may still work)
- a decent graphical card with DXT/S3TC support for gta-vc and gta-sa
- GL_EXT_texture_env_combine driver extension for displaying reflection maps correctly in opengl graphical driver
- gfx card should have at least 4 texture units for multitexturing
- one MB of disk space per installation
- windows 2000 or xp or 2003, win98 untested (may work, maybe not..)
- currently no testing was made on windows vista, if it doesn't work don't use vista.
- should run under linux / wine
- reactos is not yet at stable enough version for ggmm to work ;)

________________________________________________________________________________

Changes
________________________________________________________________________________

Version 2.3C build: 070207:
- fixed installer drag&drop bug and wrong work in progress tab being shown by default accidently
- fixed vice-city and gta3 wheel rendering
- fixed calculation of zoom level for models created with zmodeler

Version 2.3B build: 050207:
- fixed text parsing routines to handle tab characters properly.

Version 2.3 build: 200107:
- fixed search box.

Version 2.3 build: 200107:

- fixed: various internal bugs have been fixed which have not caused specific large-scale troubles
- added: visually improved car list & find box to blend with interface
- added: when viewing models, it automaticly selects ideal zoom
- added: you can change heading of car's front wheels.

Version 2.1 build: 25030X:

- fixed: vicecity and gta3 wheels now again work properly
- fixed: program will no longer render additional objects under hirerarchy root, only first object that it finds, this is also how gta does it.
- added: program now doesnt use 100% cpu usage, it will now only use so many cpu cycles as it needs to.
- added: detects and warns about corrupt txd files
- added: file dialogs in manual car installer are now resizable (thanks to Scuanor for noticing it)

Version 2.0 build: 11020X:

- added: shows cars in custom colors you wish - for car designers
- added: car view by default rotate and animate until used, this is done so that people dont think that cars are just pictures ;) you can right click and click animate to put it into animate mode at any time.
- added: + and - numpad keys now also control zoom (for those without mouse wheel and notebook users)

Version 1.7 build: 270805:

- added: some work was done on internal data editor, but it is not availible in this release.

- fixed: SA BMX now renders properly
- fixed: VC Flatbed now renders properly
- fixed: changed tractor and combine big wheel hack so now only tractor and combine have big wheels
- fixed: carmods.dat issuse should be fixed altrough i was unable to reproduce this error.

Version 1.5 build: 140805:

- added: additional handling lines like for helicopters and bikes are now supported in GGMM packages and manual car installer
- added: hirerarchy items now have checkboxes which you can uncheck and ggmm won't draw that object branch, this works with dummies too, also a note that this won't work right always, sometimes special rules apply on how gta draws things (like san andreas wheels) and so for some objects it might not work
- added: you can now control orientation of misc_a and misc_b objects
- added: you can now package weapons, but the packages don't contain weapon.dat information
- added: you can make backups of weapons
- added: the program checks if it is installed properly, if not it gives you hints on how to install it.
- added: if you on manual car installer enter colors data for car that has no color information the color information will be ADDED to colors file.

- fixed: vicecity helicopters no longer have wheels on them
- fixed: vicecity bikes now have proper wheel sizes
- fixed: you can no longer "edit" text displayed when installing ggm mods
- fixed: if you left some data to the manual car installer empty the validation mistakenly cleared some fields, now it doesn't do this anymore.


Version 1.4b (080805):
- added: option to show dummies (best viewed in wireframe mode because dummies are always drawn solid)
- added: option to disable reflections completely (sometimes the chrome is too shiny, and sometimes ATI cards couldn't handle it properly)

- fixed: solid faces no longer cut through transparent faces (and opposite). the program now draws model in 2 passes, there could be still glitches if your car happens to have transparent wheels..
- fixed: in gta3 some cars had a dummy named "steeringwheel_dummy" and GGMM accidently drawn a wheel on the dummy because it thought it is a wheel dummy, now it doesn't do that anymore.


Version 1.4a (070805):
- added: refreshes data after manual car installing
- added: propeller blades and bike wheels now also animate
- added: you can now do a little car "show-off" using object rotations in model information window (open doors, etc..)


Version 1.4 (060805):
- added: new improved program look / skin by Tank
- added: manual car installer has a validate button, the configuration is also validated when you click install button.
- added: in san andreas now shows chrome reflections (used by Linerunner, some cars and some boats) (requires GL_EXT_texture_env_combine opengl extension to look properly)
- added: in san andreas mode you can now view second uv map (may be little glitchy) (requires GL_EXT_texture_env_combine opengl extension to look properly)
- added: shininess specular sphere-maps are now displayed (in san andreas) but not in vice city yet (requires GL_EXT_texture_env_combine opengl extension to look properly)

- fixed: zmodeler 1.x cars show their normals correctly now.


Version 1.3a (050805):
- added: icons to menus and hirerarchy viewer (blue things are dummies, silver are geometry objects)
- added: model details window now shows amout of triangles and vertices rendered
- added: right clicking on car list now selects the car before showing popup menu
- added: car popup menu has a item for instant backup creation for any car

- fixed: zmodeler2 dffs now load properly
- fixed: if san andreas wheel object was not named wheel or wheel2 then it was not rendered, now the program uses object under wheel_rf_dummy for san andreas wheels just like the game does.


Version 1.3 (040805):
- added: gta3 and vice city cars now show with wheels
- added: cars are shown shiny using normals from the cars themseles
- added: program can read gta-vc speca and san andreas reflection maps (altrough i don't know how to use them properly so they would look like ingame)

- fixed: no more missing cars and wierd objects, cars are displayed the way they should without need for reloading
- fixed: every time you reloaded the car list was filled with doubles, now it doesn't do that anymore
- fixed: gta3 car rendering now works properly
- fixed: sometimes you could see thru cars where transparent objects were, now in those cases the transparency is not displayed so the view is better altrough this needs a proper object sorting fix

opposite of the features added & fixed this version of program is now actually smaller than before!


Version 1.2 (030805):
- added: backup system, when you first time install a package the original car will be packaged and put into CarBackups folder which will be created - note that when using manual car installer no backups are made because program doesn't know which car you are installing (because you can for example install data line for landstalker, dff file for infernus and txd for tank..)
- added: carmods.dat file packaging support, packages and program are ofcourse backwards compatible just that older versions will not know how to handle carmods line and will skip that data when installing ggm files
- added: more safety checking when installing .ggm mods

- fixed: sometimes if you didn't enter IDE line into manual car installer the san andreas game wasn't properly detected


Version 1.1 (020805):
- added: search box, while you type text the text the program automaticly searches the list and selects first item that contains the searched text
- added: several checks for detecting if gta game is running in background which may cause problems
- added: more checking when installing .ggm mods
- added: drag & drop on main window, you can drag & drop a ggm file into main window to install it.

- fixed: window flickering while resizing has been eliminated
- fixed: cars with 4 colors in carcols.dat now show 3 colors correctly (prim, sec, ter..), color 4 is never used afaik so i don't know how to use it


________________________________________________________________________________

Tips
________________________________________________________________________________

- you can specify coll file in manual car installer for san andreas too, if you do that it will be merged with dff model, if dff already has a coll chunk it will replace it.
- altrough main window is oddly-shaped it is resizable
- you can also view weapon models (no packaging availible yet)
- mods are packaged together with description / readme text
- the browser doesn't work yet but it will download and install mods one day
- the program works for gta3, vice city and san andreas
- the GGM files are already pretty well compressed and contain a readme.txt text that is displayed when installing mods, so you shouldn't double compress the ggm files to archieve better compression (rar might gain approx 10 kb) or to include a readme file.

________________________________________________________________________________

Known problems
________________________________________________________________________________

- The mod browser doesn't work (yet)
- 3D renderer's background sometimes doesn't look nice when the window is resized
- when resizing the window the model is not displayed until you drop the sizing grip, this problem is not too serious but i hope to fix it one day.
- the model is sometimes not rendered right, just reload the model (may take several times)
- no wheels are rendered in vice city and gta3 mode, you will see red boxes instead.

________________________________________________________________________________

Credits
________________________________________________________________________________

The program was programmed in 2005 by Jernej L. (Delfi) for www.GTAGarage.com
my website is: http://www.gtatools.com' 

Tech support: jernej@gtatools.com' + #13 +

Big Thanks to everyone that supports my work, especially these people:

Tank for the program''s design
Steve M. for his patience and help on dff format
Kcow for his DFF / TXD loader!
And big thanx to Fred for GTAGarage!!  
```

Awwwwwww, useful :3 What else?

Now, we know am .exe file is pure machine codes, zeros and ones and blah blah blah... But take a look at plain ASCII chars inside of it:

```shell
┌──(user㉿dhcppc4)-[~/Desktop/books/MMGG]
└─$ strings GGMM.exe | head -n 30
This program must be run under Win32
UPX0
@&'>
UPX1
.rsrc
2.01
UPX!
Boolean
True
Char?
SmNlint
I$eger
'Word
Str,g
Wide
TObject
IUnknown
TWrfaceI
%X"K
PLHD
@<84
0,d(
yrrr
Gn''
u:hD
moL;
hZ]_
$+ [
C2w;;g
thsz
```

Interesting stuff in head of it! Probably a bit Delfish maybe?! (I know 0 of Delfi), can't show the whole of strings if you don't wanna have hell of a long list.

Let's see the tail:

```shell
┌──(user㉿dhcppc4)-[~/Desktop/books/MMGG]
└─$ strings GGMM.exe | tail -n 50
!G#i
~mFfh/
FG=,
kfe<od
5X9qST
        \*y
Upp7
AA)7
6* ]4
[0UX
CODE
BSS
@t"WPndJ
PNe<o
)/GI
XPTPSW
+uW9
)r^I
PiU?
yrV;
        sR2
KERNEL32.DLL
advapi32.dll
comctl32.dll
comdlg32.dll
gdi32.dll
glu32.dll
gtainterface.dll
ole32.dll
oleaut32.dll
opengl32.dll
shell32.dll
user32.dll
version.dll
LoadLibraryA
GetProcAddress
VirtualProtect
ExitProcess
RegFlushKey
ImageList_Add
ChooseColorA
SaveDC
gluPerspective
IMGAddFile
IsEqualGUID
GetErrorInfo
glEnd
DragFinish
GetDC
VerQueryValueA
```
My goodness, my goodness the tail is more interesting!

These might be the list of DLLs which the program is calling:
```
KERNEL32.DLL
advapi32.dll
comctl32.dll
comdlg32.dll
gdi32.dll
glu32.dll
gtainterface.dll
ole32.dll
oleaut32.dll
opengl32.dll
shell32.dll
user32.dll
version.dll
```

and these are probably the name of the functions:
```
LoadLibraryA
GetProcAddress
VirtualProtect
ExitProcess
RegFlushKey
ImageList_Add
ChooseColorA
SaveDC
gluPerspective
IMGAddFile
IsEqualGUID
GetErrorInfo
glEnd
DragFinish
GetDC
VerQueryValueA
```

Guessing that bcuz They are `cammelCased`!
