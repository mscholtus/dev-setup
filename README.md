# Clean macOS development setup

## Setup macOS and software

- FileVault, disable iCloud unlock
- Disable data sharing
- Disable Siri
- Setup iCloud later

### Setup 1Password

- Download [1Password](https://1password.com/downloads/mac/)
- Setup accounts by scanning QR-code on iPhone
- Login to Apple iCloud
- Check and install any available updates
- Setup browser extensions

### Download software

- [Chrome](https://www.google.com/intl/nl_nl/chrome/)
- [Docker](https://www.docker.com/products/docker-desktop)
- [Firefox Developer](https://www.mozilla.org/en-US/firefox/all/#product-desktop-developer)
- [Firefox](https://www.mozilla.org/en-US/firefox/all/#product-desktop-release)
- [Spotify](https://www.spotify.com/nl/download/mac/)
- [Visual Studio Code](https://code.visualstudio.com/)

### App Store

- Affinity Designer
- Magnet
- MindNode
- NordVPN
- Slack
- The Unarchiver
- Things
- Reeder (setup Safari extension)
- Wipr (setup Safari extension)

--------

## Development setup

### Homebrew

- [Setup instructions](https://1password.com/downloads/mac/)

- `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`
- XCode command line tools will be installed

### Setup packages

- `brew install node`
- `brew cask install iterm2`
- `npm install -g n`

### Visual Studio Code

- Run command: Install 'code' command in path
- Install [One Dark Pro](https://marketplace.visualstudio.com/items?itemName=zhuangtongfa.Material-theme)
- Install [Fire Code](https://github.com/tonsky/FiraCode/releases)

Settings.json
```json
{
    "workbench.colorTheme": "One Dark Pro",
    "editor.fontFamily": "Fira Code, 'Courier New', monospace",
    "editor.fontLigatures": "'ss02', 'ss08', 'zero'"
}
```

### iTerm 2

[One Dark theme](https://github.com/one-dark/iterm-one-dark-theme)

Go to iTerm2 -> Profiles -> Colors -> Color presets… -> One Dark
Go to iTerm2 -> Profiles -> Text -> Font -> Fira Code Retina
Go to iTerm2 -> Preferences -> Advanced and scroll to the Drawing section, then change:

`Improves drawing performance at the expense of disallowing alphanumeric characters to belong to ligatures.` to `No`

### Zsh + Oh My Zsh