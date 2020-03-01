# General Configurations for Desktop Linux

## Automatic Keyboard Configuration

On keyboard settings select 'Use system defaults'

Execute the commands
```
sudo dpkg-reconfigure keyboard-configuration
sudo reboot
```

## Start Menu Configuration

Execute the commands
```
sudo apt install alacarte
```

Run alacarte GUI and add the menu items that you wish

## Copy/Paste from terminal

Execute the commands
```
sudo apt install xclip
```

Add the following line to your ~/.bashrc o ~/.zshrc
```
alias pbcopy='xclip -selection clipboard'
alias pbpaste='xclip -selection clipboard -o'
```
 
Example
```
ls | pbcopy
```

