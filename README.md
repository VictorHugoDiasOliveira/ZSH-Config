# ZSH-Config

## Install ZSH
```
sudo apt install zsh
```

## Define ZSH as default terminal
```
chsh -s $(which zsh)
```

## Install dependencies
```
sudo apt install curl git -y
```

## Install OhMyZSH (restart your system)
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Download NerdFont JetBrains Mono
- https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/JetBrainsMono.zip

## Move it for fonts folder
```
sudo cp *.ttf /usr/share/fonts/
```

## Install Hyper
- https://hyper.is/#installation

## Changing Settings
- Open Hyper -> Settings -> Edit -> Preferences

## Copy this settings and paste then on preferences
- https://github.com/HunnTeRUS/my-nvim-configuration/blob/master/hyper-terminal-config.hyper.js

## Install SpaceShip theme for OhMySZH
```
git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
```

## Create a symlink for theme
```
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
```

## Auto Complete and Highlight
- ZSH Auto Suggestions
```
git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```
- ZSH Syntax Highlighting
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```

## Edit ~/.zshrc
```
sudo nano ~/.zshrc
```
- Add this Code and don't forget to comment the default theme line
```
ZSH_THEME="spaceship"
SPACESHIP_CHAR_SUFFyIX=" "

source $ZSH/oh-my-zsh.sh

source $ZSH_CUSTOM/plugins/zsh-autosuggestions/zsh-autosuggestions.zsh
source $ZSH_CUSTOM/plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```
- Reload ZSH
```
source ~/.zshrc
```

## Possible problems:
Hyper wasn't Opening, so after trying to open Hyper using command line it returned me a problem with chrome-sandbox, you can solve it using the following command:
```
sudo chmod 4755 /opt/Hyper/chrome-sandbox
```

After seting sources at ~/.zshrc i got some errors when opening terminal, i solved them moving the sources to the end of the file.
