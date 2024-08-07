# macOS

## Homebrew

### Install Homebrew

https://brew.sh/

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Install Formulae

```bash
brew update
brew install bash \
    deno \
    emacs \
    gh \
    gnupg \ 
    golang \
    haskell-stack \
    kubernetes-cli \
    neovim \
    ocaml \
    pinentry-mac \
    podman \
    tmux
```

### Install Casks

```bash
brew update
brew install --cask \
    alacritty \
    brave-browser \
    chromium \
    contour \
    cool-retro-term \
    discord \
    docker \
    duckduckgo \
    firefox \
    font-0xproto-nerd-font \
    font-bigblue-terminal-nerd-font \
    font-commit-mono-nerd-font \
    font-fira-mono-nerd-font \
    font-geist-mono-nerd-font \
    font-go-mono-nerd-font \
    font-hack-nerd-font \
    font-hasklug-nerd-font \
    font-liberation-nerd-font \
    font-monaspace-nerd-font \
    font-noto-nerd-font \
    font-sauce-code-pro-nerd-font \
    font-terminess-ttf-nerd-font \
    gimp \
    google-chrome \
    hyper \
    iterm2 \
    kitty \
    postman \
    proton-drive \
    proton-mail \
    proton-pass \
    protonvpn \
    rectangle \
    vscodium
```

## Neovim

```bash
gh repo clone george-greene/kickstart.nvim "${XDG_CONFIG_HOME:-$HOME/.config}"/nvim
nvim
```

## Rust

https://www.rust-lang.org/tools/install

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

## NVM

https://github.com/nvm-sh/nvm

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

## Bun

https://bun.sh/

```bash
curl -fsSL https://bun.sh/install | bash
```
