
# theme-collection-xfwm4


* [theme-collection-xfwm4](https://github.com/samwhelp/theme-collection-xfwm4)


## clone

``` sh
$ git clone https://github.com/samwhelp/theme-collection-xfwm4.git
```


## themes

### Pastel

| Pastel |
| --- |
| [Pastel_Dark](themes/Pastel_Dark) |
| [Pastel_Dark_NoTitle](themes/Pastel_Dark_NoTitle) |
| [Pastel_Light](themes/Pastel_Light) |
| [Pastel_Light_NoTitle](themes/Pastel_Light_NoTitle) |

### RGaps

| RGaps |
| --- |
| [RGapsBlack](themes/RGapsBlack) |
| [RGapsBlackNoButtons](themes/RGapsBlackNoButtons) |
| [RGapsBlend](themes/RGapsBlend) |
| [RGapsBlendNoButtons](themes/RGapsBlendNoButtons) |
| [RGapsLine](themes/RGapsLine) |
| [RGapsLineNoButtons](themes/RGapsLineNoButtons) |

> www.gnome-look.org / XFWM4 Themes / [RGaps](https://www.gnome-look.org/p/1174081/)

> note-about-manjaro / Theme / [RGaps](https://samwhelp.github.io/note-about-manjaro/read/theme/source/rgaps.html)

> note-about-ubuntu / Theme / [RGaps](https://samwhelp.github.io/note-about-ubuntu/read/theme/source/rgaps.html)

## doc

* [https://wiki.xfce.org/howto/xfwm4_theme](https://wiki.xfce.org/howto/xfwm4_theme)
* [https://en.wikipedia.org/wiki/X_PixMap](https://en.wikipedia.org/wiki/X_PixMap)

## themes directory

### System Global

* /usr/share/themes/
* /usr/local/share/themes

### Personal Local

* ~/.local/share/themes
* ~/.themes


```
find /usr/share/themes/ -name xfwm4
find /usr/local/share/themes -name xfwm4
find ~/.local/share/themes -name xfwm4
find ~/.themes/ -name xfwm4
```


## Install Xfwm4 Theme Tool

* [xfce4-appearance-settings](https://manpages.ubuntu.com/manpages/bionic/en/man1/xfce4-appearance-settings.1.html) (Package: [xfce4-settings](https://packages.ubuntu.com/bionic/xfce4-settings)) (GUI)
* [appearance-install-theme](https://packages.ubuntu.com/bionic/amd64/xfce4-settings/filelist) (Package: [xfce4-settings](https://packages.ubuntu.com/bionic/xfce4-settings)) (CLI)
* [xfwm4-theme-ctrl](xfwm4-theme-ctrl) (CLI) (My Script)

## Set Xfwm4 Theme Tool

* [xfwm4-settings](https://manpages.ubuntu.com/manpages/bionic/en/man1/xfwm4-settings.1.html) (GUI)
* [xfconf-query](https://manpages.ubuntu.com/manpages/bionic/en/man1/xfconf-query.1.html) (CLI) (channel: xfwm4) (property: /general/theme)
* [xfce4-settings-editor](https://manpages.ubuntu.com/manpages/bionic/en/man1/xfce4-settings-editor.1.html) (GUI) (channel: xfwm4) (property: /general/theme)

## Config File

* ~/.config/xfce4/xfconf/xfce-perchannel-xml/xfwm4.xml



## Install theme by xfce4-appearance-settings

### Step

1. Launch xfce4-appearance-settings.
2. Drag theme_directory or theme_archive, then drop to xfce4-appearance-settings.

> install theme to [~/.themes]

## Install theme by appearance-install-theme

### How to find appearance-install-theme

run

``` sh
dpkg -L xfce4-settings | grep appearance-install-theme
```

or run

``` sh
dpkg -L xfce4-settings | grep install
```

show

```
/usr/lib/x86_64-linux-gnu/xfce4/settings/appearance-install-theme
```

### How to install theme by appearance-install-theme

Ex: install [themes/Pastel_Dark] to [~/.themes]

run

``` sh
/usr/lib/x86_64-linux-gnu/xfce4/settings/appearance-install-theme 'themes/Pastel_Dark'
```

or run

``` sh
$(dpkg -L xfce4-settings | grep appearance-install-theme) 'themes/Pastel_Dark'
```

## Install theme by [xfwm4-theme-ctrl](xfwm4-theme-ctrl)


### help

run

``` sh
$ ./xfwm4-theme-ctrl
```

or run

``` sh
$ ./xfwm4-theme-ctrl help
```

show

```
Usage:
	$ xfwm4-theme-ctrl [action]

	$ xfwm4-theme-ctrl list

	$ xfwm4-theme-ctrl install {name}

	$ xfwm4-theme-ctrl install_all

	$ xfwm4-theme-ctrl now [name]


Example:

	## help

	$ xfwm4-theme-ctrl
	$ xfwm4-theme-ctrl help


	## available to install

	$ xfwm4-theme-ctrl list


	## install

	$ xfwm4-theme-ctrl install 'Pastel_Dark'
	$ xfwm4-theme-ctrl install 'Pastel_Dark_NoTitle'
	$ xfwm4-theme-ctrl install 'Pastel_Light'
	$ xfwm4-theme-ctrl install 'Pastel_Light_NoTitle'

	$ xfwm4-theme-ctrl install_all


	## get current

	$ xfwm4-theme-ctrl now


	## set current

	$ xfwm4-theme-ctrl now 'Pastel_Dark'
	$ xfwm4-theme-ctrl now 'Pastel_Dark_NoTitle'
	$ xfwm4-theme-ctrl now 'Pastel_Light'
	$ xfwm4-theme-ctrl now 'Pastel_Light_NoTitle'

Debug:
	$ export DEBUG_THEME_CTRL=true

```

### show available theme list

run

``` sh
./xfwm4-theme-ctrl list
```

show

```
Pastel_Dark
Pastel_Dark_NoTitle
Pastel_Light
Pastel_Light_NoTitle
```

### install single theme

ex: install themes/Pastel_Dark

run

``` sh
$ ./xfwm4-theme-ctrl install 'Pastel_Dark'
```

### install all theme

run

``` sh
$ ./xfwm4-theme-ctrl install_all
```

### get current xfwm4 theme

run

``` sh
$ ./xfwm4-theme-ctrl now
```

### set current xfwm4 theme

run

``` sh
$ ./xfwm4-theme-ctrl now  'Pastel_Dark'
```


## Other Tool

* [style-de-xfce](https://github.com/samwhelp/play-ubuntu-18.04-plan/tree/master/prototype/style-de/xfce)
* [style-switch-xfce](https://github.com/samwhelp/play-ubuntu-18.04-plan/tree/master/project/style-tool/xfce/style-switch)
* [style-ctrl-xfce](https://github.com/samwhelp/play-ubuntu-18.04-plan/tree/master/project/style-tool/xfce/style-ctrl)
