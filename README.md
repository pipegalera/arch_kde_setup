# arch_setup





https://aur.archlinux.org/brave-bin.git


- Update the system: pacman -Syu
- Download Wallpapger from https://basicappleguy.com/

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
```


## Latte-dock ??

https://github.com/KDE/latte-dock/blob/master/INSTALLATION.md
