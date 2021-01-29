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

## Finder

Create development and screenshots folder and save screenshots to this folder:

```bash
mkdir ~/Development
mkdir ~/Documents/Screenshots/
defaults write com.apple.screencapture location ~/Documents/Screenshots && killall SystemUIServer
```

- Add `home` and `~/Development` folders to sidebar

### Download software

- [Chrome](https://www.google.com/intl/nl_nl/chrome/)
- [Docker](https://www.docker.com/products/docker-desktop)
- [Firefox Developer](https://www.mozilla.org/en-US/firefox/all/#product-desktop-developer)
- [Firefox](https://www.mozilla.org/en-US/firefox/all/#product-desktop-release)
- [Spotify](https://www.spotify.com/nl/download/mac/)
- [Visual Studio Code](https://code.visualstudio.com/)

--------

## Development setup

### Homebrew

- [Setup instructions](https://1password.com/downloads/mac/)

- `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`
- XCode command line tools will be installed

### Setup packages

```bash
brew install node
brew cask install iterm2
npm install -g n diff-so-fancy
```
- [n](https://www.npmjs.com/package/n)
- [diff-so-fancy](https://www.npmjs.com/package/diff-so-fancy) setup:
```bash
git config --global core.pager "diff-so-fancy | less --tabs=4 -RFX"
git config --global color.ui true
git config --global color.diff-highlight.oldNormal    "red bold"
git config --global color.diff-highlight.oldHighlight "red bold 52"
git config --global color.diff-highlight.newNormal    "green bold"
git config --global color.diff-highlight.newHighlight "green bold 22"
git config --global color.diff.meta       "11"
git config --global color.diff.frag       "magenta bold"
git config --global color.diff.commit     "yellow bold"
git config --global color.diff.old        "red bold"
git config --global color.diff.new        "green bold"
git config --global color.diff.whitespace "red reverse"
```

### Git/ssh keys setup

```bash
git config --global user.name "Your Name Here"
git config --global user.email "your_email@youremail.com"
```
- Setup ssh keys in Github and Bitbucket accounts. [Guide](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

### Visual Studio Code

- Run VS code command: `Install 'code' command in path`
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

- Go to iTerm2 -> Profiles -> Colors -> Color presets… -> One Dark
- Go to iTerm2 -> Profiles -> Text -> Font -> Fira Code Retina
- Go to iTerm2 -> Preferences -> Advanced and scroll to the Drawing section, then change:
    - `Improves drawing performance at the expense of disallowing alphanumeric characters to belong to ligatures.` to `No`
- Go to iTerm2 -> Appearance -> General -> Theme -> Minimal

### Zsh + Oh My Zsh

```bash
brew install zsh
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
- Plugins: `plugins=(git colored-man-pages colorize brew osx zsh-syntax-highlighting zsh-autosuggestions z)`

### Keyboard and mouse setup

- Download [Logi Options](https://www.logitech.com/nl-nl/product/options) for Logitech MX Master 3
- Download [VIA](https://caniusevia.com) for Idobao ID80V2 mechanical keyboard
- If keyboard needs to be flashed, load `via/idobao_id80v2.json` VIA config.