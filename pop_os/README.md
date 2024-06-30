# Pop!_OS

## Brave Browser

https://brave.com/linux/

```bash
sudo apt install curl

sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list

sudo apt update

sudo apt install brave-browser
```

## GitHub CLI

https://github.com/cli/cli/blob/trunk/docs/install_linux.md

```bash
(type -p wget >/dev/null || (sudo apt update && sudo apt-get install wget -y)) \
&& sudo mkdir -p -m 755 /etc/apt/keyrings \
&& wget -qO- https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo tee /etc/apt/keyrings/githubcli-archive-keyring.gpg > /dev/null \
&& sudo chmod go+r /etc/apt/keyrings/githubcli-archive-keyring.gpg \
&& echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
&& sudo apt update \
&& sudo apt install gh -y
```

## APT Packages

There are a number of programs that can be installed using the `apt` package manager.

```bash
sudo apt install alacritty \
    tmux \
    vim \
    emacs \
    bat \
    ripgrep
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

## Neovim

APT has an out-of-date Neovim package, so install from releases on GitHub.

```bash
curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim-linux64.tar.gz
sudo rm -rf /opt/nvim
sudo tar -C /opt -xzf nvim-linux64.tar.gz
```

Then add to `~/.bashrc`:

```bash
export PATH="$PATH:/opt/nvim-linux64/bin"
```

## Proton

### Mail & Calendar

Download from website: https://proton.me/mail/download

### Pass

Download from website: https://proton.me/pass/download

### VPN

https://protonvpn.com/support/official-linux-vpn-ubuntu/

```bash
wget https://repo.protonvpn.com/debian/dists/stable/main/binary-all/protonvpn-stable-release_1.0.3-3_all.deb

sudo dpkg -i ./protonvpn-stable-release_1.0.3-3_all.deb && sudo apt update

echo "de7ef83a663049b5244736d3eabaacec003eb294a4d6024a8fbe0394f22cc4e5  protonvpn-stable-release_1.0.3-3_all.deb" | sha256sum --check -

sudo apt install proton-vpn-gnome-desktop

sudo apt update && sudo apt upgrade

sudo apt install libayatana-appindicator3-1 gir1.2-ayatanaappindicator3-0.1 gnome-shell-extension-appindicator
```
