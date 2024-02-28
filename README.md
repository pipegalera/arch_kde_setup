# 🚧 arch_setup 🚧


## TBD 

1. Atuin: https://github.com/atuinsh/atuin
2. https://github.com/ajeetdsouza/zoxide
3. Alacritty install and configure
4. Install VLC or MPV
5. Set up Autologin

`sudo nano /etc/gdm/custom.conf`

AutomaticLoginEnable=True
AutomaticLogin=[YourUsername]

5. Grub-reboot
6. Temps monitor: https://www.reddit.com/r/kde/comments/13bf8ym/how_to_get_something_similar_to_vitals_for_gnome/

## Distro 

https://endeavouros.com/

I installed it with KDE Plasma desktop env and without any GPU drivers. Once the distro its installed, I installed the GPU drivers (I needed NVIDIA beta drivers that do not ship with Calamares). 

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

- **Kvantum Theme engine**

https://github.com/tsujan/Kvantum/tree/master/Kvantum

```
sudo pacman -S kvantum
```

- **Sonora KDE Theme**

https://github.com/vinceliuice/MacSonoma-kde

```
https://github.com/vinceliuice/MacSonoma-kde
cd MacSonoma-kde
./install.sh --round
```

- **WhiteSur Theme**

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

- **WhiteSur Icon Theme**

https://github.com/vinceliuice/WhiteSur-icon-theme

```
git clone https://github.com/vinceliuice/WhiteSur-icon-theme.git
cd WhiteSur-icon-theme
./install.sh -a
```

- **WhiteSur Cursors**

https://github.com/vinceliuice/WhiteSur-cursors

```
git clone https://github.com/vinceliuice/WhiteSur-cursors.git
cd WhiteSur-cursors
./install.sh
```

- **Lightly Theme**

https://github.com/Luwx/Lightly

```
sudo pacman -S cmake extra-cmake-modules kdecoration qt5-declarative qt5-x11extras
yes | yay -S lightly-git
```

- **Fonts**

```
git clone https://github.com/pipegalera/arch_setup.git
cd arch_setup
unzip fonts.zip -d ~/.local/share
ls -al ~/.local/share/fonts
```

- **Walpaper**

Download any Wallpapger from https://basicappleguy.com/. They are awesome. 

- **Settings**

```
- Apperance -> Global Theme -> MacSonoma-Dark
- Apperance -> Application Style -> Lightly
- Apperance -> Application Style -> Configure GNOME/GTK Application Style -> GTK theme: WhiteSure-Dark
- Apperance -> Window Decorations -> Window border size -> No borders
- Apperance -> Window Decorations -> Titlebar Buttons -> Only X, up-arrow, down-arrow. (all at the left) 
- Apperance -> Fonts -> Adjust all fonts -> SF Pro Display
- Apperance -> Fonts -> Fixed width -> FiraCode Nerd Mono
- Workspace Behaviour -> Screen Looking -> The one that you like.
- Startup and Shutdown -> Login Screen (SDDM) -> MacSonoma-Dark
```

## Applications

```
yes | yay -S timeshift-autosnap
yes | yay -S vscodium-bin
yes | yay -S flameshot-git
yes | yay -S brave-bin
yes | yay -S apostrophe
```

## Python Environment Manager

```
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
~/miniconda3/bin/conda init bash
~/miniconda3/bin/conda init zsh
```

- **Create environment for preprocessing (Rapids)**

https://rapids.ai/cudf-pandas/

```
conda create --solver=libmamba -n rapids -c rapidsai -c conda-forge -c nvidia rapids=23.12 python=3.10 cuda-version=12.0 pytorch
```

- **Create environment for deep learning (Pytorch 2.0)**

https://pytorch.org/get-started/pytorch-2.0/

```
conda create -n pytorch2 python
conda activate pytorch2
pip3 install numpy --pre torch torchvision torchaudio --force-reinstall --index-url https://download.pytorch.org/whl/nightly/cu118
```


## Link Github account

```
conda install gh --channel conda-forge	
gh auth login
git config --global user.email "pipegalera@gmail.com"
git config --global user.name "Pipe Galera"
```

Test that `gh repo list` displays all your repos. 


## VS Code / VS Codium configuration 

- **Change copy&paste behaviour**

1. File > Preferences > Keyboard Shortcuts
2. Search for "Terminal:Copy" and "Terminal:Paste" and change them for "Crtl+C" and "Crtl+V"



