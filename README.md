# Configs

<br/><br/>

## Arrow keys to JKLM on Ubuntu 24.04

### 1. No Wayland 

When you log in for the first time, ensure that you're not using Ubuntu Wayland. Check the bottom-right corner and choose ubuntu (X11)

### 2. Create the keybinding file in the home directory 

```bash
touch .xmodmap
```

Fill it with the keybindings (French keyboard): 
```
keycode 66 = Mode_switch
keycode 44 = j J Left
keycode 46 = l L Right
keycode 45 = k K Up
keycode 47 = m M Down
```

### 3. Create the executable file 

```bash
touch .xmodmap.sh
```

Fill it with this simple command : 
```
xmodmap ~/.xmodmap
```

### 4. Permission 
```bash
sudo chmod +x ~/.xmodmap.sh
```

### 5. Startup application 

Create a startup application with this command inside : 
```bash
sh -c "$HOME/.xmodmap.sh"
```
<br/><br/>

## Custom shorcut Ubuntu 

super + T => `gnome-terminal --maximize`

<br/><br/>

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
