# 1. Mac Configuration

- [1. Mac Configuration](#1-mac-configuration)
  - [1.1. Description](#11-description)
  - [1.2. Instructions](#12-instructions)
    - [1.2.1. Settings](#121-settings)
    - [1.2.2. Install Appications](#122-install-appications)
    - [1.2.3. Make Symlinks](#123-make-symlinks)
    - [1.2.4. Configure Applications](#124-configure-applications)
      - [1.2.4.1. 1Password](#1241-1password)
      - [1.2.4.2. Magnet](#1242-magnet)
      - [1.2.4.3. Spark](#1243-spark)
      - [1.2.4.4. VSCode](#1244-vscode)
      - [1.2.4.5. Obsidian](#1245-obsidian)
      - [1.2.4.6. Fish](#1246-fish)
      - [1.2.4.7. iTerm](#1247-iterm)
  - [1.3. To-do](#13-to-do)

## 1.1. Description
I enjoy having a really clean setup on my MacOS devices, but I also like to experiment a lot.  
This causes me to reinstall my devices from scratch a lot, so this here is just a summary of all commands and tasks for reinstalling my setup. It might change a lot over time. 

This is not really made to be super useful for anyone else, but might give others some ideas when looking at it. 

---

## 1.2. Instructions
### 1.2.1. Settings
|                                         Description | Command                                                                                                                            |
| --------------------------------------------------: | ---------------------------------------------------------------------------------------------------------------------------------- |
|                              Set background picture | `osascript -e 'tell application "Finder" to set desktop picture to POSIX file "/System/Library/Desktop Pictures/The Cliffs.heic"'` |
|        Set automatic rearranging of spaces to false | `defaults write com.apple.dock mru-spaces -bool false`                                                                             |
|          Set keyboard shortcuts for changing spaces | `Unknown`                                                                                                                          |
|          Set Safari default password manager to off | `Unknown`                                                                                                                          |
| Set touch bar to always show extended control strip | `defaults write com.apple.touchbar.agent PresentationModeGlobal -string fullControlStrip; killall ControlStrip`                    |
|              Set Finder to always show hidden files | `defaults write com.apple.finder AppleShowAllFiles -bool YES; killall Finder`                                                      |
|                                  Set TrackPad speed | `defaults write -g com.apple.trackpad.scaling -float 1.5`                                                                          |
|                       Set three finger drag to true | `defaults write com.apple.AppleMultitouchTrackpad TrackpadThreeFingerDrag -bool true`                                              |
|                       Set Dock orientation to right | `defaults write com.apple.dock orientation right; killall Dock`                                                                    |
|                      Set Dock magnification to true | `defaults write com.apple.dock magnification -bool true; killall Dock`                                                             |
|                              Set size of Dock icons | `defaults write com.apple.dock tilesize -float 16; killall Dock`                                                                   |
|                     Set magnification of Dock icons | `defaults write com.apple.dock largesize -float 128; killall Dock`                                                                 |
|                      Set Dock to automatically hide | `defaults write com.apple.dock autohide -bool true; killall Dock`                                                                  |
|           Set Dock to only show active applications | `defaults write com.apple.dock static-only -bool true; killall Dock`                                                               |

---

### 1.2.2. Install Appications
1. Install Homebrew: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
2. Generate ssh key and add at it GitHub: `ssh-keygen -t ed25519 -a 100`
3. Clone this repository: `git clone git@github.com:TerjeLafton/mac-configuration.git` 
4. Enter the repository: `cd mac-configuration`
3. Write `brew bundle` to install all applications in the Brewfile

---

### 1.2.3. Make Symlinks
| Application | Command                                                      |
| ----------: | ------------------------------------------------------------ |
|         Git | `ln -s ~/Projects/mac-configuration/.gitconfig ~/.gitconfig` |

---

### 1.2.4. Configure Applications
#### 1.2.4.1. 1Password
1. Enable the Safari extension

#### 1.2.4.2. Magnet
1. Allow accessibility access in privacy settings
2. Enable launch at logon

#### 1.2.4.3. Spark
1. Sign in with terje@lafton.io to sync all settings

#### 1.2.4.4. VSCode
1. Sign in to settings sync with GitHub account and all extensions and settings will be synced
2. Install Cartograph CF font fomr iCloud Drive

#### 1.2.4.5. Obsidian
1. Open the Notes vault from iCloud Drive. All settings will be synced and extensions automatically downloaded

#### 1.2.4.6. Fish
1. Run `fish`in the terminal to start the fish shell
2. Add `/usr/local/bin/fish` to the `/etc/shells`
3. Set Fish as the default shell: `chsh -s /usr/local/bin/fish`
4. Run `fish_config``
    1. Set theme: Tomorrow
    2. Set prompt: Arrow

#### 1.2.4.7. iTerm
1. Set font: Cartograph CF
2. Enable ligatures
3. Set cursor: vertical bar
4. Set theme: itermTheme.itemcolors

---

## 1.3. To-do
[ ] Create install script  
[ ] Create sync script for dotfiles
