# Configs

## Arrow keys to JKLM on Ubuntu 24.04

### 1. No Wayland 

When you log in for the first time, ensure that you're not using Ubuntu Wayland. Check the bottom-right corner and choose ubuntu 

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

## Custom shorcut Ubuntu 

super + T => `gnome-terminal --full-screen`
