# MMGG
GGMM reverese engeering!

I think I'm not allowed to put original files here, but I can give you a link:

https://www.gtagarage.com/mods/show.php?id=434

and I will put my REVENGed files of GGMM, I call it MMGG project :3

I already mailed initial and original programmer and recieved no answers, metdata shows he's been offline for like 15 years! I hope he's still alive!
________________________________

Ok... It's my first time that I wanna back engineer sth, never done it before!

Alright here we are, in a directory with following files:

```shell
┌──(user㉿dhcppc4)-[~/Desktop/books/MMGG]
└─$ ls
GGMM.exe  GGMM.txt  GTAINTERFACE.dll
    
```

I know that the program was created using Delfi lang, and I know nothing of Delfi, but I think it's safe to stick into standard procedure, Which is scanning the file types:3

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

Now, we know a .exe file is pure machine codes, zeros and ones and blah blah blah... But take a look at plain ASCII chars inside of it:

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

Now... Using this `strings GGMM.exe | awk '{ print length(), $0 | "sort -n" }'` I wanna see what are the biggest plain ASCII bytes (together) in thsi file:

```shell
┌──(user㉿dhcppc4)-[~/Desktop/books/MMGG]
└─$ strings GGMM.exe | awk '{ print length(), $0 | "sort -n" }' | tail -n 50
11 :    ssRegul6x
11 ta|J;BS#W,|
11 ThreadArray
11 ufXcn mvOmI
11 version.dll
12 = $8570]RGBe
12 23456789ABCD
12 advapi32.dll
12 ChooseColorA
12 comctl32.dll
12 comdlg32.dll
12 D~vcltest3%l
12 GetErrorInfo
12 G    FuchsiaAqu
12 HIwJh[Db`8"O
12 KERNEL32.DLL
12 |lf_Wspl7wg_
12 LoadLibraryA
12 ;~N|*p}&|~")
12 oleaut32.dll
12 opengl32.dll
12 ORGB = %.3d
12 QTm3SC=3JQ^6
12 !_reicobmpz\
12 v3$- *-&*$Q{
12 V_c]%&G#Av9X
12 XiiazzJzZJAA
13 ABORTRETRYIGB
13 ImageList_Add
13 v0?  TBiDiMode
14 GetProcAddress
14 gluPerspective
14 #t&<0t%<.t,<,t
14 VerQueryValueA
14 VirtualProtect
15 b]5SUBTRAC%_0`-
15 ?NYGOMG! 16 bit
15  "yTXT"maK+e9am
16 ANSI_CHARSETDEFA
16 g.deg#^$+Q<VV>9-
16 gtainterface.dll
22 Fel32.dllgGetDiskFreeL
31 ortions Copyright (c) 1983,97 B
31 ''''pqrs''''tuvw''''xyz{''''|}~
36 This program must be run under Win32
48 |x9999tplh9999d`\X9999TPLH9999D@<8999940,(9999$ 
48 |x9999tplh9999d`\X9999TPLH9999D@<8999940,(9999$ 
48 |xNNNNtplhNNNNd`\XNNNNTPLHNNNND@<8NNNN40,(NNNN$ 
48 |x''''tplh''''d`\X''''TPLH''''D@<8''''40,(''''$ 
152 ''''`abc''''defg''''hijk''''lmno''''PQRS''''TUVW''''XYZ[''''\]^_''''@ABC''''DEFG''''HIJK''''LMNO''''0123''''4567''''89:;''''<=>?'''' !"#''''$%&'''''()*+
```

Impressing stuff!

To start with these 152 byes `''''abc''''defg''''hijk''''lmno''''PQRS''''TUVW''''XYZ[''''\]^_''''@ABC''''DEFG''''HIJK''''LMNO''''0123''''4567''''89:;''''<=>?'''' !"#''''$%&'''''()*+` represent the alphabet and digits.

And that `Copyright (c) 1983,97` is so bloody scary!!

Now let's look for all the .dll names we can see in plain string:

```shell
┌──(user㉿dhcppc4)-[~/Desktop/books/MMGG]
└─$ strings GGMM.exe | grep -i "dll"                                        
Fel32.dllgGetDiskFreeL
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
just Fel32.dll was missing.

________________________________

Interesting command `strings` is ey...!? Let's do the same to `GTAINTERFACE.dll` :

```shell
┌──(user㉿dhcppc4)-[~/Desktop/books/MMGG]
└─$ strings GTAINTERFACE.dll
This program must be run under Win32
CODE
`DATA
.idata
.edata
P.reloc
P.rsrc
StringX
TObjectd
TObjectX
System
IUnknown
System
u:hD
SVWUQ
Z]_^[
SVWU
YZ]_^[
SVWU
]_^[
SVWU
w;;t$
]_^[
SVWU
]_^[
SVWUQ
Z]_^[
SVWU
YZ]_^[
SVWU
uW;{
u:;{
]_^[
ZYYd
ZYYd
SVWU
YZ]_^[
YZ^[
SVWU
]_^[
ZYYd
_^[YY]
QSVW
ZYYd
_^[Y]
SVWU
$;L$
$)D$
YZ]_^[
QSVW
UhE%@
ZYYd
hL%@
_^[Y]
YZXu
        w,9
2_^[
Uha(@
ZYYd
hh(@
SOFTWARE\Borland\Delphi\RTL
FPUMaskValue
PPRTj
YYZX
VWUd
SPRQ
T$(j
SVWU
]_^[
ZTUWVSPRTj
]_^[
d$,1
,t\=
t=HtN
r6t0
t.Ht
Ph).@
ZYYd
_^[]
Uhn/@
ZYYd
_^[]
SVWU
Portions Copyright (c) 1983,97 Borland
]_^[
;_^[
SVWU
PSUj
PSUj
]_^[
t!R:
t-Rf;
t f;J
SVRP
Z^[X
uXJt
uAJt
u:Jt
It%S
t&J|
;_^[
PSVW
_^[X
_^[X
SVWU
]_^[
]_^[
SVWU
]_^[
]_^[
SVWU
PSWj
PSWj
]_^[
SVWU
UWVSj
]_^[
r*PRf
Uh =@
ZYYd
h'=@
ZYYd
h+?@
u^f=
ZYYd
h+?@
ZYYd
Software\Borland\Locales
Software\Borland\Delphi\Locales
ZYYd
_^[YY]
UhXE@
ZYYd
h_E@
Ht Ht.
F$TF@
F $F@
F$$F@
F 'F@
wHQj
HXYu
C$wJ@
u3YX
u'ZX
|HtE=
,U M@
,UVN@
,U M@
,UVN@
@v:k
@aQY
E@|o
BkU'9
USVW3
_^[]
USVW
_^[]
USVW3
_^[]
USVW
_^[]
Uh6R@
ZYYd
h=R@
Uh(S@
ZYYd
h/S@
u*PR
Uh1U@
ZYYd
h8U@
Uh      W@
ZYYd
ZYYd
        Exception
EHeapException
EOutOfMemory
EInOutError
        EExternal
EExternalException
        EIntError
EDivByZero
ERangeErrorX]@
EIntOverflow
EMathError
EInvalidOp
EZeroDivide
        EOverflow
EUnderflow
EInvalidPointer
EInvalidCast
EConvertError
EAccessViolation
EPrivilege
EStackOverflow
        EControlC
EVariantError
EAssertionFailed
EAbstractError
EIntfCastError
EWin32Error
TActiveThreadArray
$TMultiReadExclusiveWriteSynchronizer
SVWQ
PWVS
$Z_^[
SVWQ
PWVS
$Z_^[
SVWU
]_^[
SVW3
Uhsg@
ZYYd
hzg@
_^[YY]
(_^[
9w7k
_^[[
_^[]
SVWQ
Z_^[
QSVW
_^[Y]
SVW3
Uh>q@
ZYYd
hEq@
_^[]
QSVW
_^[Y]
UhQr@
PhLq@
ZYYd
hXr@
Uh!t@
ZYYd
h(t@
_^[Y]
yyyy
eeee
D$HPj
Uh&w@
ZYYd
h-w@
_^[Y]
        TErrorRec
ZYYd
TExceptRec
SVW3
ZYYd
h#y@
ZYYd
,tY=
t<HtH
r3t7
t(Ht
ZYYd
ZYYd
ZYYd
SVWU
F       j*
t@Uj
]_^[
QQQQQS3
ZYYd
m/d/yy
mmmm d, yyyy
 AMPM
AMPM 
:mm:ss
ZYYd
kernel32.dll
GetDiskFreeSpaceExA
N(;F,t
@v:k
INFNANU
QS<$t
$*@@@*$@@@$ *@@* $@@($*)@-$*@@$-*@@$*-@@(*$)@-*$@@*-$@@*$-@@-* $@-$ *@* $-@$ *-@$ -*@*- $@($ *)(* $)U
@WVS
u f=
<'t$<"t 
<#t&<0t%<.t,<,t3<'t5<"t1<Et:<et6<;tF
<#t'<0t#<.t
<Et$<et <;tS
ZYYd
ZYYd
ZYYd
ZYYd
ZYYd
False
True
ZYYd
EStreamError
EFCreateError
EFOpenErrorL
EFilerError
EReadError
EWriteErrorT
EListError
EStringListError
TList
TThreadList
TPersistent
TPersistent
Classes
IStringsAdapter
Classes
TStrings
TStrings
Classes
TStringItem
TStringListH
TStringList
Classes
TStream
THandleStream
TFileStream
TCustomMemoryStream`
TMemoryStream
ZYYd
ZYYd
^[Y]
YZ^[
ZYYd
^[Y]
ZYYd
^[Y]
ZYYd
^[Y]
ZYYd
ZYYd
SVW3
ZYYd
SVW3
|-F3
W8CNu
ZYYd
ZYYd
ZYYd
[YY]
Strings
SVW3
|0F3
ZYYd
YZ^[
SVW3
ZYYd
ZYYd
ZYYd
SVW3
ZYYd
SVW3
|#C3
ZYYd
QSVW
S$_^[Y]
ZYYd
ZYYd
ZYYd
^[YY]
SVW3
ZYYd
ZYYd
_^[YY]
SVWU
]_^[
ZYYd
ZYYd
ZYYd
ZYYd
^[Y]
ZYYd
^[Y]
ZYYd
ZYYd
[YY]
SVW3
ZYYd
SVW3
ZYYd
_^[YY]
ZYYd
^[Y]
ZYYd
_^[Y]
SVWU
]_^[
ZYYd
_^[Y]
ZYYd
^[Y]
$Z^[
ZYYd
_^[Y]
Rp_^[
ZYYd
_^[Y]
ZYYd
_^[Y]
SVW3
ZYYd
ZYYd
^[YY]
SVW3
ZYYd
ZYYd
SVW3
ZYYd
_^[Y]
SVWU
~,;{
]_^[
ZYYd
_^[YY]
QSVW
ZYYd
_^[Y]
ZYYd
ZYYd
^[Y]
ZYYd
ZYYd
ZYYd
ZYYd
_^[]
ZYYd
ZYYd
.dir
.img
SVW3
ZYYd
.img
SVW3
$ZXr
ZYYd
replacing
file exists, proceeding...
bigger file
.img
smaller or same file
ZYYd
[YY]
QQQQSVW3
|6C3
$ZXv
ZYYd
.img
header + dir size: 
file 0 is at : 
first img block is occupied by : 
 at 
RELOCATING first img block that is occupied by : 
gtadll
VER2
.dir
_^[]
ZYYd
ZYYd
Runtime error     at 00000000
Error
0123456789ABCDEF                                                                
kernel32.dll
GetCurrentThreadId
DeleteCriticalSection
LeaveCriticalSection
EnterCriticalSection
InitializeCriticalSection
VirtualFree
VirtualAlloc
LocalFree
LocalAlloc
VirtualQuery
WideCharToMultiByte
MultiByteToWideChar
lstrlenA
lstrcpyA
LoadLibraryExA
GetThreadLocale
GetStartupInfoA
GetModuleFileNameA
GetLocaleInfoA
GetLastError
GetCommandLineA
FreeLibrary
ExitProcess
WriteFile
SetFilePointer
SetEndOfFile
RtlUnwind
ReadFile
RaiseException
GetStdHandle
GetFileSize
GetFileType
CreateFileA
CloseHandle
user32.dll
GetKeyboardType
LoadStringA
MessageBoxA
advapi32.dll
RegQueryValueExA
RegOpenKeyExA
RegCloseKey
oleaut32.dll
VariantChangeTypeEx
VariantCopyInd
VariantClear
SysStringLen
SysFreeString
SysReAllocStringLen
SysAllocStringLen
kernel32.dll
TlsSetValue
TlsGetValue
TlsFree
TlsAlloc
LocalFree
LocalAlloc
GetModuleFileNameA
kernel32.dll
WriteFile
WaitForSingleObject
VirtualQuery
SetFilePointer
SetFileAttributesA
SetEndOfFile
ReadFile
OutputDebugStringA
LeaveCriticalSection
InitializeCriticalSection
GlobalUnlock
GlobalReAlloc
GlobalHandle
GlobalLock
GlobalFree
GlobalAlloc
GetVersionExA
GetThreadLocale
GetTempPathA
GetProcAddress
GetModuleHandleA
GetModuleFileNameA
GetLocaleInfoA
GetLastError
GetDiskFreeSpaceA
GetCurrentThreadId
GetCPInfo
FormatMessageA
FindFirstFileA
FindClose
FileTimeToLocalFileTime
FileTimeToDosDateTime
EnumCalendarInfoA
EnterCriticalSection
DeleteFileA
DeleteCriticalSection
CreateFileA
CreateEventA
CompareStringA
CloseHandle
user32.dll
MessageBoxA
LoadStringA
GetSystemMetrics
DestroyWindow
GTAINTERFACE.dll
IMGAddFile
IMGDelete
IMGExportFile
IMGFileCount
IMGGetThisFile
IMGLoadImg
IMGReDoDir
IMGRemoveFile
IMGReplaceFile
IMGSetThisFile
0,080<0@0D0H0L0P0T0`0m0
1&1.161>1F1N1V1^1f1n1v1~1
2"2*222;2\2d2
4'5:5
556i6u6
6#7r8
9#919D9N9T9b9h9p9
: :+:<:B:J:T:k:v:
:.;D;
<#=)=B=K=T=_=h=o=~=
>"?(?8?A?
040N0x0
1,121D1\1h1p1
2H2l2
3,353
4-535;5^5v5
8=8S8j8
;6;^;|;
>=>_>
>/?B?V?
0c0h0
1#1+101C1H1V1
1A2_2u2
4!4,4<4C4
5&52595
:&:}:
:@;r;
212G2S2a2h2o2u2|2
3#3:3B3J3R3Z3b3j3|3
3 4(464<4V4g4
5,5>5F5N5V5^5f5n5v5~5
6&6.666>6F6N6V6^6f6n6v6~6
7$7,747<7D7L7T7\7d7l7t7|7
8$8,848<8D8L8T8\8d8l8t8|8
9$9,949<9D9L9T9\9d9l9t9|9
:*:<:\:d:h:l:p:t:x:|:
; ;$;(;,;0;4;8;<;L;l;t;x;|;
<$<,<0<4<8<<<@<D<H<L<\<|<
=,=4=8=<=@=D=H=L=P=T=h=
>8>@>D>H>L>P>T>X>\>`>p>
? ?@?H?L?P?T?X?\?`?d?h?|?
0 040T0\0`0d0h0l0p0t0x0|0
1 1$1(1,10141H1h1p1t1x1|1
2$2(2,2024282<2@2D2\2|2
343<3@3D3H3L3P3T3X3\3x3
5j5u5
7"7f7
9z;~;
B0Z0_0k0
011V1
222D2x2
2-3X3q3~3
4%5*525\5m5v5-6;6X6a6
7X7o7
848P8W8`8
9Q:x:
:];o;
= =/=9=>=D=I=O=T=Z=a=g=l=r=w=}=
>4>=>F>O>T>
S0i0
1)1<1E1d1r1
2(272E2h2
4#424L4~4
485,6064686<6@6D6H6L6P6T6X6\6`6d6h6l6p6t6x6|6
7 7$7,70787<7D7H7P7T7\7`7h7l7t7x7
8 8(8,84888@8D8L8P8X8\8d8h8p8t8|8
;/;`;|>
2)232>2H2S2]2h2r2|2
3"3H3k3w3
4$4,4;4G4T4f4
5 5$5(5,5054585L5l5t5x5|5
6 6(6,6064686<6@6D6H6X6x6
7(7074787<7@7D7H7L7P7`7
8$8D8L8P8T8X8\8`8d8h8l8|8
9-9L9X9\9l9t9x9|9
:$:2:6:H:a:l:|:
; ;$;(;,;0;4;D;U;Y;l;
< <$<(<<<\<d<h<l<p<t<x<|<
=4=<=@=D=H=L=P=T=X=\=`=d=h=l=p=
>->2>
>8?[?r?
0?0g0
122a2
2)3}3
3T4j4
747J7
8D8{8%9`9
:3:b:x:
;+;o;
<N<s<
=R>o>
0&1=1_1
1N2e2
4*5A5t5
727A7X7
8)8]8l8
:q;};
< </<t<y<
0;0?0C0G0K0O0S0W0[0_0c0g0k0o0s0w0
18162>2K2W2f2
3"3<3H3M3_3r3z3
4$4+494b4p4
5.5A5L5n5
6%6*696L6f6
677B7l7
8-8^8y8
9'9;9b9
9o:{:
;d;p;
<(<B<Z<j<|<
=@=g=z=
>?>Q?a?m?
0004080<0@0D0H0L0P0T0X0\0`0d0h0l0p0t0x0|0
0,1014181<1@1D1H1L1P1T1X1\1`1d1h1l1p1t1x1|1
2$2,242<2D2L2T2\2d2l2t2|2
3 3$3(3,3034383<3@3D3H3L3P3T3X3\3`3d3h3l3p3t3x3|3
4 4$4(4,4044484<4@4D4H4L4P4
AAAAX
"(X(""X
ss""
--"""8
"X""sssr
)G~9B9JAN
6b)Z
6b.4)
#1!))
{{{!Z
{{{!Z
{{{!Z
sss.e
-RRcZZZ
)G~;y
9B9369_l_sss1
++3k{
_l_4CV
R[oc{k
{{{x
ZZZFJ^J
N^N++3
kkkZZZZZZZZZZZZZZZZZZZZZ
!!x{
R[oZZZZZZBFJZ
R[o)9J-/T
sssZ
99cUMl
kkkp
R[oR[o
R=c{`
JAN++3JRZJRZ
-)9J
)Z-/T
ZRcBDT
!B)Jk
R=cZcs
!RJRZ%N
cZsR=c
ckkRRcZO
BDT)!B
5{)G~
369sR
ZcskV
FJ^99c
!R)G~
!ANsg
Vk{9Rc
--/T
-^%N
++3cs
#1ZRc
Vk{++3
!)))9JBDT
369ZcsZcsZcs
1JZss)9JZcsZcsZcs++3
&=O8
GTAINTERFACE
Consts
System
SysInit
QTypInfo
SysUtils
KWindows
SysConst
sActiveX
3Messages
^Classes
```

That is just terrific :3 Sooo much data and metadata*-*

Important stuff:

* `This program must be run under Win32`
* `SOFTWARE\Borland\Delphi\RTL`
* `Portions Copyright (c) 1983,97 Borland`
* `Software\Borland\Locales`
* `Software\Borland\Delphi\Locales`
* `Exception` `EHeapException` `EOutOfMemory` `EInOutError` `EExternal` `EExternalException` `EIntError` `EDivByZero` `ERangeErrorX` `EIntOverflow` `EMathError` `EInvalidOp` `EZeroDivide` `EOverflow` `EUnderflow` `EInvalidPointer` `EInvalidCast` `EConvertError` `EAccessViolation` `EPrivilege` `EStackOverflow` `EControlC` `EVariantError` `EAssertionFailed` `EAbstractError` `EIntfCastError` `EWin32Error` `TActiveThreadArray`
* `$TMultiReadExclusiveWriteSynchronizer`
* `TErrorRec` `TExceptRec`
* `GetDiskFreeSpaceExA`
*  `EStreamError`
`EFCreateError`
`EFOpenErrorL`
`EFilerError`
`EReadError`
`EWriteErrorT`
`EListError`
`EStringListError`
`TList`
`TThreadList`
`TPersistent`
`TPersistent`
`Classes`
`IStringsAdapter`
`Classes`
`TStrings`
`TStrings`
`Classes`
`TStringItem`
`TStringListH`
`TStringList`
`Classes`
`TStream`
`THandleStream`
`TFileStream`
`TCustomMemoryStream`
`TMemoryStream`

 * And some messages: `replacing` `file exists, proceeding...` `bigger file` `smaller or same file` `header + dir size:` `file 0 is at :` `first img block is occupied by :` `RELOCATING first img block that is occupied by :` `Runtime error     at 00000000` 
 * `GetCurrentThreadId` `DeleteCriticalSection` `LeaveCriticalSection` `EnterCriticalSection` `InitializeCriticalSection` `VirtualFree` `VirtualAlloc` `LocalFree` `LocalAlloc` `VirtualQuery` `WideCharToMultiByte` `MultiByteToWideChar` `lstrlenA` `lstrcpyA` `LoadLibraryExA` `GetThreadLocale` `GetStartupInfoA` `GetModuleFileNameA` `GetLocaleInfoA` `GetLastError` `GetCommandLineA` `FreeLibrary` `ExitProcess` `WriteFile` `SetFilePointer` `SetEndOfFile` `RtlUnwind` `ReadFile` `RaiseException` `GetStdHandle` `GetFileSize` `GetFileType` `CreateFileA` `CloseHandle` `user32.dll` `GetKeyboardType` `LoadStringA` `MessageBoxA` `advapi32.dll` `RegQueryValueExA` `RegOpenKeyExA` `RegCloseKey` `oleaut32.dll` `VariantChangeTypeEx` `VariantCopyInd` `VariantClear` `SysStringLen` `SysFreeString` `SysReAllocStringLen` `SysAllocStringLen` `kernel32.dll` `TlsSetValue` `TlsGetValue` `TlsFree` `TlsAlloc` `LocalFree` `LocalAlloc` `GetModuleFileNameA` `kernel32.dll` `WriteFile` `WaitForSingleObject` `VirtualQuery` `SetFilePointer` `SetFileAttributesA` `SetEndOfFile` `ReadFile` `OutputDebugStringA` `LeaveCriticalSection` `InitializeCriticalSection` `GlobalUnlock` `GlobalReAlloc` `GlobalHandle` `GlobalLock` `GlobalFree` `GlobalAlloc` `GetVersionExA` `GetThreadLocale` `GetTempPathA` `GetProcAddress` `GetModuleHandleA` `GetModuleFileNameA` `GetLocaleInfoA` `GetLastError` `GetDiskFreeSpaceA` `GetCurrentThreadId` `GetCPInfo` `FormatMessageA` `FindFirstFileA` `FindClose` `FileTimeToLocalFileTime` `FileTimeToDosDateTime` `EnumCalendarInfoA` `EnterCriticalSection` `DeleteFileA` `DeleteCriticalSection` `CreateFileA` `CreateEventA` `CompareStringA` `CloseHandle` `user32.dll` `MessageBoxA` `LoadStringA` `GetSystemMetrics` `DestroyWindow` `GTAINTERFACE.dll` `IMGAddFile` `IMGDelete` `IMGExportFile` `IMGFileCount` `IMGGetThisFile` `IMGLoadImg` `IMGReDoDir` `IMGRemoveFile` `IMGReplaceFile` `IMGSetThisFile`
* `GTAINTERFACE`
* `Consts`
`System`
`Consts
System
SysInit
QTypInfo
SysUtils
KWindows
SysConst
sActiveX
3Messages
^ClassesSysInit`
`QTypInfo`
`SysUtils`
`KWindows`
`SysConst`
`sActiveX`
`3Messages`
`^Classes`

________________________________________________

So far, so cool :3

But let's wind the clock back a bit! Remember when we first scanned whole directory we executed `file *` and it led us into:

```
GGMM.exe:         PE32 executable (GUI) Intel 80386, for MS Windows, UPX compressed
```

right? now there are important infos about file like `UPX compressed` or `PE32 executable (GUI) Intel 80386`.

Staring with `UPX compressed` :

https://en.wikipedia.org/wiki/UPX says : 
> UPX (Ultimate Packer for Executables) is a free and open source executable packer supporting a number of file formats from different operating systems.


and we've got `upx` command as well:

```shell
┌──(user㉿dhcppc4)-[~/Desktop/books/MMGG]
└─$ upx                                           
                       Ultimate Packer for eXecutables
                          Copyright (C) 1996 - 2020
UPX 3.96        Markus Oberhumer, Laszlo Molnar & John Reiser   Jan 23rd 2020

Usage: upx [-123456789dlthVL] [-qvfk] [-o file] file..

Commands:
  -1     compress faster                   -9    compress better
  -d     decompress                        -l    list compressed file
  -t     test compressed file              -V    display version number
  -h     give more help                    -L    display software license
Options:
  -q     be quiet                          -v    be verbose
  -oFILE write output to 'FILE'
  -f     force compression of suspicious files
  -k     keep backup files
file..   executables to (de)compress

Type 'upx --help' for more detailed help.

UPX comes with ABSOLUTELY NO WARRANTY; for details visit https://upx.github.io

```

SO I am going to make a copy of our .exe file and unpack it:
```shell
┌──(user㉿dhcppc4)-[~/Desktop/books/MMGG]
└─$ cp GGMM.exe GGMM_unpacked.exe
                                                                                                                                                                                                                                           
┌──(user㉿dhcppc4)-[~/Desktop/books/MMGG]
└─$ upx -d GGMM_unpacked.exe 
                       Ultimate Packer for eXecutables
                          Copyright (C) 1996 - 2020
UPX 3.96        Markus Oberhumer, Laszlo Molnar & John Reiser   Jan 23rd 2020

        File size         Ratio      Format      Name
   --------------------   ------   -----------   -----------
   1039360 <-    446976   43.00%    win32/pe     GGMM_unpacked.exe

Unpacked 1 file.
                                                                                                                                                                                                                                           
┌──(user㉿dhcppc4)-[~/Desktop/books/MMGG]
└─$ 

```
