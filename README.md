# iTerm2 & zsh installation guide
---

## Example

![Alt text](/iterm-example.png?raw=true "Screenshot")

---

## How to install iTerm2
### macOS
Download iTerm from web [ https://www.iterm2.com/ ] or using Homebrew 
```
brew cask install iterm2
```

## How to install ZSH
### macOS
Try zsh --version before installing it from Homebrew. If it's newer than 4.3.9 you might be OK. Preferably newer than or equal to 5.0.
```
brew install zsh zsh-completions
```

## Install FiraCode Fonts
- Download: [ https://github.com/tonsky/FiraCode/releases/download/1.206/FiraCode_1.206.zip ]

- How to install: [ https://github.com/tonsky/FiraCode/wiki ]

## ZSH config:
Clone repo and then copy zsh to .config

## After that you can configure your ZSH
ZSH needs to ZDOTDIR to work properly, so you need to create file zshenv in /etc directory, just run this command:
```
sudo sh -c echo 'export ZDOTDIR=${HOME}/.config/zsh' > /etc/zshenv
```
After you need to add zsh to your shells:
```
sudo sh -c "echo '/usr/local/bin/zsh' >> /etc/shells"
```
Last ste is to change your default shell to ZSH:
```
chsh -s /usr/local/bin/zsh
exec zsh
```

---
## Installing iTerm2 tools and plugins
Steps below will guide you to make better iTerm look and more user friendly

Auto setup
* Optionally, backup your existing `~/.config/zsh` [`cp ~/.config/zsh ~/.config/zsh.backup`] before changes
* Override folder `zsh`
* Run command `exec zsh`

Additional imports
* Import theme for iTerm called `Solarized Dark theme` [ https://gist.github.com/kevin-smets/8568070 ]. Just go iTerm → preferences → profiles → colors → load presets.
* Import `profile-config.json` in your profiles in iTerm, this step will override your window settings, so be aware
* Customize `.zshrc` and `.zshenv` to your needs..
* Test if everything is working correctly, run command `exec zsh` and reopen iTerm

---
## Further changes

If you want to have fancy `cat` command look, just install `ccat` from Homebrew
```
brew install ccat
```

Optional step
Also install Prezto — Instantly Awesome Zsh [ https://github.com/sorin-ionescu/prezto ]
