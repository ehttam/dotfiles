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

## SUCKLESS DWM ON UBUNTU 
Lenovo ThinkPad T14s AMD

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

### FSCREENSHOT

```
$ sudo apt install flameshot
$ mkdir -p ~/Pictures/screenshots
$ sudo chmod 777 ~/Pictures/screenshots
$ sudo ln -s /home/dotefiles/XXX/bin/fscreenshot /usr/bin/fscreenshot
``` 

### TOUCHPAD
activate natural scrolling
https://www.topbug.net/blog/2017/02/23/enable-natural-scrolling-for-trackpads-using-libinput/

```
$ xinput 
$ xinput --list
$ xinput --list-props "ETPS/2 Elantech Touchpad"
$ xinput --set-prop "ETPS/2 Elantech Touchpad" "libinput Natural Scrolling Enabled" 1
```

--> ~/.xinitrc
```
# activate tapping
xinput set-prop "ETPS/2 Elantech Touchpad" "libinput Tapping Enabled" 1
# activate natural scrolling
xinput set-prop "ETPS/2 Elantech Touchpad" "libinput Natural Scrolling Enabled" 1
# speed up touchpad
xinput set-prop "ETPS/2 Elantech Touchpad" "libinput Accel Speed" 0.4
```
### TRACKPOINT
slow down trackpoint speed

--> ~/.xinitrc
```
# slow down trackpoint speed
xinput set-prop "ETPS/2 Elantech TrackPoint" "libinput Accel Speed" -0.5
``` 

### SCREEN / DISPLAY TEARING
--> ~/.xinitrc
```
xrandr --auto
...
# picom & # try fix tearing
xrandr --output eDP --set TearFree on
``` 

### DARK THEME GLOBALLY

If you're not using gnome or xfce but have some gtk apps installed then you could always set your theme preferences.
Edit the file `~/.config/gtk-3.0/settings.ini` and set `gtk-application-prefer-dark-theme=1` 
Edit the file `~/.config/gtk-4.0/settings.ini` and set `gtk-application-prefer-dark-theme=1` 

``` 
[Settings]
gtk-theme-name=Nordic-master
gtk-application-prefer-dark-theme=0
``` 

https://www.youtube.com/watch?v=3jvFpYaSoPo
https://varunbpatil.github.io/2013/09/28/dwm.html
