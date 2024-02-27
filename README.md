# arch_setup

## Distro 

https://endeavouros.com/ , non NVIDIA version (GPU currently only works under Beta NVIDIA linux drivers).

## First boot

```
pacman -Syu
yay --save --answerdiff None --answerclean None --removemake
```

## Update to beta Linux drivers

https://github.com/Frogging-Family/nvidia-all


```
git clone https://github.com/Frogging-Family/nvidia-all.git
cd nvidia-all
makepkg -si
```

## Activate Bluetooth 

```
sudo systemctl start bluetooth
sudo systemctl enable bluetooth
```

## Personalization 

https://www.youtube.com/watch?v=jWDgdC28tYo

### Kvantum Theme engine

https://github.com/tsujan/Kvantum/tree/master/Kvantum

```
sudo pacman -S kvantum
```

### Sonora KDE Theme

https://github.com/vinceliuice/MacSonoma-kde

```
https://github.com/vinceliuice/MacSonoma-kde
cd MacSonoma-kde
./install.sh --round
```

### WhiteSur Theme

https://github.com/vinceliuice/WhiteSur-gtk-theme

```
git clone https://github.com/vinceliuice/WhiteSur-gtk-theme.git --depth=1
cd WhiteSur-gtk-theme
./install.sh
```

For the Maclike log in screen: 

```
cd ..
cd sddm
./install.sh
```

### WhiteSur Icon Theme

https://github.com/vinceliuice/WhiteSur-icon-theme

```
git clone https://github.com/vinceliuice/WhiteSur-icon-theme.git
cd WhiteSur-icon-theme
./install.sh -a
```

### WhiteSur Cursors

https://github.com/vinceliuice/WhiteSur-cursors

```
git clone https://github.com/vinceliuice/WhiteSur-cursors.git
cd WhiteSur-cursors
./install.sh
```

### Lightly Theme

https://github.com/Luwx/Lightly

```
sudo pacman -S cmake extra-cmake-modules kdecoration qt5-declarative qt5-x11extras
yay -S lightly-git
```

### Fonts

``
git clone https://github.com/pipegalera/arch_setup.git
cd arch_setup
unzip fonts.zip -d ~/.local/share
ls -al ~/.local/share/fonts
```

### Walpaper

Download any Wallpapger from https://basicappleguy.com/. They are awesome. 

### Settings


- Apperance -> Global Theme -> MacSonoma-Dark
- Apperance -> Application Style -> Lightly
- Apperance -> Application Style -> Configure GNOME/GTK Application Style -> GTK theme: WhiteSure-Dark
- Apperance -> Window Decorations -> Window border size -> No borders
- Apperance -> Window Decorations -> Titlebar Buttons -> Only X, up-arrow, down-arrow. (all at the left) 
- Apperance -> Fonts -> Adjust all fonts -> SF Pro Display
- Apperance -> Fonts -> Fixed width -> FiraCode Nerd Mono
- Workspace Behaviour -> Screen Looking -> The one that you like.
- Startup and Shutdown -> Login Screen (SDDM) -> MacSonoma-Dark

## Latte-dock ??

https://github.com/KDE/latte-dock/blob/master/INSTALLATION.md

## Applications

```
 
```




