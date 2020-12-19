# DOTFILES **arch**pad

## CLONE REPO
```
$ git clone ...
```

### CREATE SYMLINKS
```
$ ln -s ....
``` 

e.g.

```
$ ln -s ~/dotfiles/vim/vimrc.symlink ~/.vimrc
```

## SUCKLESS DWM

```
$ sudo apt-get install build-essential libx11-dev libxinerama-dev sharutils suckless-tools

$ git clone https://git.suckless.org/dwm ~/dotfiles/suckless/dwm

$ sudo make clean install
```

Ubuntu Display Manager gdm3
```
$ sudo apt install dwm
$ sudo mv /usr/share/xsessions/dwm.desktop /usr/share/xsessions/dwm.desktop.bak
$ sudo apt purge dwm
$ sudo mv /usr/share/xsessions/dwm.desktop.bak /usr/share/xsessions/dwm.desktop
```

```
Desktop Entry]
Encoding=UTF-8
Name=Dwm
Comment=Dynamic window manager
# Exec=dwm
Exec=/home/matthe/.xinitrc
Icon=dwm
Type=XSession

```

### Brightness Button
```
$ sudo vim /etc/sudoers
```
-->
```
%sudo   ALL=(ALL) NOPASSWD:/home/matthe/dotfiles/bin/brightness
%sudo   ALL=(ALL) NOPASSWD:/sys/class/backlight/amdgpu_b10/brightness
```

### fscreenshot

```
$ sudo apt install flameshot
$ mkdir -p ~/Pictures/screenshots
$ sudo chmod 777 ~/Pictures/screenshots
$ sudo ln -s /home/dotefiles/XXX/bin/fscreenshot /usr/bin/fscreenshot
``` 

### touchpad
Natural Scrolling aktiviernen
https://www.topbug.net/blog/2017/02/23/enable-natural-scrolling-for-trackpads-using-libinput/

```
$ xinput 
$ xinput --list
$ xinput --list-props "ETPS/2 Elantech Touchpad"
$ xinput --set-prop "ETPS/2 Elantech Touchpad" " libinput Natural Scrolling Enabled" 1
```

--> ~/.xinitrc
```
 xinput --set-prop "ETPS/2 Elantech Touchpad" "libinput Natural Scrolling Enabled" 1
```



