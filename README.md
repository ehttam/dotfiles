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

```$ ln -s ~/dotfiles/vim/vimrc.symlink ~/.vimrc
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


