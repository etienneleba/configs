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
