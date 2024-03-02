# 🚧 arch_setup 🚧




## Distro 

https://endeavouros.com/

I installed it with KDE Plasma desktop env and without any GPU drivers. Once the distro its installed, I installed the GPU drivers (I needed NVIDIA beta drivers that do not ship with Calamares). 

## First boot

```
pacman -Syu
yay --save --answerdiff None --answerclean None --removemake
```

- Adjust the window layout manager by pressing `SUPER + t`

## Autologin 

- Startup and Shutdown -> Login Screen (SDDM) -> Behaviour -> Automatically log in as user, Plasma.


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

https://www.youtube.com/watch?v=z78r7FFPFuw&list=WL&index=23&t=603s


- **Fonts**

```
git clone https://github.com/pipegalera/arch_setup.git
cd arch_setup
unzip fonts.zip -d ~/.local/share
ls -al ~/.local/share/fonts
```

- **Walpaper**

Download any Wallpapger from https://basicappleguy.com/. They are awesome. 


## Applications

```
yes | yay -S timeshift-autosnap
yes | yay -S vscodium-bin
yes | yay -S flameshot-git
yes | yay -S brave-bin
yes | yay -S apostrophe
yay -S alacritty-git
yes | yay rstudio-desktop-bin
sudo pacman -S vlc
```

https://github.com/atuinsh/atuin?tab=readme-ov-file#install

```
bash <(curl https://raw.githubusercontent.com/atuinsh/atuin/main/install.sh)
atuin import auto
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


## Alacritty configuration 

```
cd .config
mkdir alacritty
touch alacritty.toml
```

