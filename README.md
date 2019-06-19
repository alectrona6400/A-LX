Platinum9.1
======

![System 9.1](https://i.imgur.com/BRUweb0.png)


> This is an expansion of the Platinum9 theme pack by @grassmunk


Installation
======

Paths are valid for a debian/ubuntu based systems running the Xfce desktop enviornment, adjust accordingly if needed.


## Icons

Copy the `NineIcons` folder into your `~/.icons` folder, or your `/usr/share/icons` folder for system-wide use.

Update your icon cache:

`gtk-update-icon-cache /home/[username]/.icons/NineIcons/`


## Cursors

Copy the `retrosmart-x11-cursors` folder to your `~/.icons/` folder.


## Theme

Copy the `ClassicPlatinumStreamlined`, `PlatiPlus` and `PlatiPlus26` folders into your `~/.themes` folder, or your `/usr/share/themes` folder for system-wide use.

Menu > Settings > Appearance

Style: `ClassicPlatinumStreamlined`

Icons: `NineIcons`

Fonts: Default Font: `Charcoal`, Size 8 / Default Monospace Font: `Monaco`, Size 11

Settings: Uncheck everything.

Menu > Settings > Window Manager

Style: `PlatiPlus`

Title Font: `Charcoal`, Size 8

Title Alignment: Center

Menu > Settings > Settings Editor > xfwm4 > Borderless Maximize: Uncheck the `Value` checkbox if it is checked.


## Wallpaper

Copy your wallpapers folder into your `~/.wallpaper` folder, or your `/usr/share/wallpaper/` folder for system-wide use.


## Fonts

Copy your font .ttf files into your `~/.fonts/truetype/` folder, or your `/usr/share/fonts/truetype/` folder for system-wide use.

Then, run the command `fc-cache -f -v` to rebuild your fonts index.


## File Manager Configuration (Thunar)

Open a folder window and activate the shortcuts `Ctrl+B` and `Ctrl+E` so that there is no side pane. Optionally, `Ctrl+M` to turn off the menu bar.


## Media Player (qmmp)

Copy the `/qmmp/mac8amp.wsz` file into your `~/.qmmp/skins/` folder. (more skins are available [here](http://qmmp.ylsoftware.com/files/skins/winamp-skins/).)


## Boot Screen (Plymouth)


Copy the `/boot/System8` folder into your `/usr/share/plymouth/themes/` folder

The following command inserts the new folder path into your default.plymouth file:

`sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/System8/System8.plymouth 100`

The following command allows you to choose from the entries in your default.plymouth file:

`sudo update-alternatives --config default.plymouth`

The following command updates initrd with new changes.

`sudo update-initramfs -u`


## Global Topmenu (vala-panel-appmenu)


The following command will bring your repository information up to date:

`sudo apt-get update`

The following command will install `vala-panel-appmenu` and its dependencies:

`sudo apt install xfce4-appmenu-plugin`

The following commands will configure `vala-panel-appmenu` to display the active applications.

`xfconf-query -c xsettings -p /Gtk/ShellShowsMenubar -n -t bool -s true`

`xfconf-query -c xsettings -p /Gtk/ShellShowsAppmenu -n -t bool -s true`

Now `AppMenu Plugin` will appear in your `Add New Panel Items` pane.



## Menu Customization


Panel > Add New Panel Items > Applications Menu

Right Click on Applications Menu > Properties

Uncheck: `Show icons in menu`, `Show application description in tooltip`, `Show button title`

Icon: `~/.icons/NineIcons/menu/apple.png` (or, /usr/share/icons...)

Panel > Add New Panel Items > Separator {Settings:Transparent}

Panel > Add New Panel Items > Applicatinons Menu

Panel > Add New Panel Items > AppMenu Plugin

Panel > Add New Panel Items > PulseAudio Plugin

Panel > Add New Panel Items > Clock

Panel > Add New Panel Items > Window Menu

Panel > Add New Panel Items > Separator {Settings:Transparent}


Sound Effects
====

`to-do`



Terminal Color Themes
====


## MATE Terminal

Font: `Monaco` Regular 7

Window: Right Click -> Menubar Off

Window: Right Click -> Preferences -> Profile Preferences

Window Width: 138px Height: 48px

Wallpaper: `~/.wallpaper/OS9-wallpaper/Finder/Mac OS Background.jpg` (or, /usr/share/wallpaper..)

Colors:

Text Color:

`#16525C`

Bold Color:

`#9959A3`


Palette Entry 0-7

`#AFB8D6`

`#FF7A21`

`#493050`

`#5B7E02`

`#AA0D69`

`#CE5C00`

`#5C3566`

`#2E3436`

Palette Entry 8-15

`#4F597C`

`#FFB17C`

`#C55E0A`

`#82974B`

`#CE7BAC`

`#C58D3D`

`#AD7FA8`

`#C0C0BD`


## GNOME Terminal

Window: Right Click -> Menubar Off

Window: Right Click -> Preferences

Font: `undefined medium` / size: 7 / line height: 1.10

Colors:

TEXT: `#FFFCD2` / `#6A6B9B`

BOLD: [on] `#B598FF`

CURSOR: [off]

HIGHLIGHT: `#FFFFFF` / `#FF0000`

Transparency: just about five percent..


Palette Entry 0-7

`#B7B7B7`

`#CE5454`

`#CC8EC4`

`#8ED5D5`

`#D0D060`

`#C98A92`

`#86BAC1`

`#E3E0EA`

`#E0E0E0 `

`#ED6161`

`#EEABE5`

`#A8F7F7`

`#FFFF77`

`#EEABB3`

`#ABE6EE`

`#D3C2F7`


Acknowledgements
====

* Theme based largely on the work of @grassmunk's Platinum9 set.
* Additional icons borrowed from the Chicago95 set by @grassmunk which can be found [here](https://github.com/grassmunk/Chicago95)
* The Chicago95_Extras expansion to this set by @grassmunk can be found [here](https://github.com/grassmunk/Chicago95_Extras).
* Global top menu is vala-panel-appmenu by @rilian-la-le and can be found [here](https://github.com/rilian-la-te/vala-panel-appmenu).
* Mac System 8 boot screen by @vladkorotnev can be found [here](https://github.com/vladkorotnev/System8).
* Classic Mac cursors are called retrosmart-x11-cursors by @mdomlop and can be found [here](https://github.com/mdomlop/retrosmart-x11-cursors).
* undefined-medium font by @andirueckel can be found [here](https://github.com/andirueckel/undefined-medium)

