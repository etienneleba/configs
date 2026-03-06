# Configs

<br/><br/>

## Arrow keys to JKLM on Ubuntu 24.04

### 1. Install keyd 

```bash
sudo apt install build-essential git
git clone https://github.com/rvaiya/keyd
cd keyd
make && sudo make install
sudo systemctl enable keyd && sudo systemctl start keyd
```

### 2. Create default file

```bash
sudo nano /etc/keyd/default.conf
```

Copy/paste the content of default.conf

### 3. Reload keyd 

```bash
sudo keyd reload
```

## Remove middle click paste 

[Tuto](https://askubuntu.com/questions/4507/how-do-i-disable-middle-mouse-button-click-paste)

## Zsh 

You need to have curl and git already installed 

### 1. Install Zsh 

```bash
sudo apt-get update
sudo apt-get install zsh 
```

### 2. Define Zsh as default shell 

```bash
chsh -s $(which zsh)
```

### 3. Install Oh My Zsh 

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### 4. Choose your theme 

Chosse your theme here : [https://github.com/ohmyzsh/ohmyzsh/wiki/themes](https://github.com/ohmyzsh/ohmyzsh/wiki/themes)

```
# .zshrc
ZSH_THEME="robbyrussell"
```

### 5. Install plugins 

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

### 6. Enable plugins 

```
# .zshrc
plugins=(git zsh-autosuggestions zsh-syntax-highlighting zsh-completions)
```

### 7. Apply changes

```bash
source ~/.zshrc
```

<br/><br/>

## Vinium 

### 1. Download Vinium extension 

Firefox : [https://addons.mozilla.org/en-US/firefox/addon/vimium-ff/](https://addons.mozilla.org/en-US/firefox/addon/vimium-ff/) <br/>
Google : [https://chromewebstore.google.com/detail/vimium/dbepggeogbaibhgnhhndojpepiihcmeb?hl=en](https://chromewebstore.google.com/detail/vimium/dbepggeogbaibhgnhhndojpepiihcmeb?hl=en)

### 2. Restore mapping 

Go in the Vinium options and upload vinium-options.json to restore the custom mapping 


<br/><br/>

## PHPStorm 

### 1. Create keymaps folder 

```bash
mkdir ~/.config/JetBrains/PhpStorm<version>/keymaps
```

### 2. Add my own keymaps 

Copy Perso.xml to keymaps folder, restart PHPStorm and choose the keybindings in the settings 

### 3. JKLM Mapping 

In order for the JKLM to arrows mapping to work, you need to check the "Use national layouts for shortcuts" box

![Screenshot from 2024-11-13 15-04-50](https://github.com/user-attachments/assets/32f80520-9049-4201-9110-4cc3e545b71d)

### 4. Setup tests with docker compose 

[Setting up PhpStorm to run PHPUnit tests inside an already running docker container](https://amandoabreu.com/wrote/setting-up-phpstorm-to-run-phpunit-tests-inside-an-already-running-docker-container/)

[Use non modal commit interface](https://intellij-support.jetbrains.com/hc/en-us/community/posts/16080207913618-Local-Changes-Tab-missing)

