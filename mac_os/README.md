# macOS

## Homebrew

### Install Homebrew

```bash
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

* Installs

Various commands for getting fresh OS installs up and running with common programs, organized by OS.

** Pop!_OS

*** Brave Browser

[[https://brave.com/linux/][Installing Brave on Linux]]

#+BEGIN_SRC bash

sudo apt install curl

sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list

sudo apt update

sudo apt install brave-browser

#+END_SRC

*** GitHub CLI

[[https://github.com/cli/cli/blob/trunk/docs/install_linux.md][Installing gh on Linux and BSD]]

#+BEGIN_SRC bash

(type -p wget >/dev/null || (sudo apt update && sudo apt-get install wget -y)) \
&& sudo mkdir -p -m 755 /etc/apt/keyrings \
&& wget -qO- https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo tee /etc/apt/keyrings/githubcli-archive-keyring.gpg > /dev/null \
&& sudo chmod go+r /etc/apt/keyrings/githubcli-archive-keyring.gpg \
&& echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
&& sudo apt update \
&& sudo apt install gh -y

#+END_SRC

*** APT Packages

There are a number of programs that can be installed using the `apt` package manager.

#+BEGIN_SRC bash

sudo apt install alacritty tmux vim neovim emacs bat ripgrep

#+END_SRC

*** Rust

[[https://www.rust-lang.org/tools/install][Install Rust]]

#+BEGIN_SRC bash

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

#+END_SRC

*** NVM

[[https://github.com/nvm-sh/nvm][Installing and Updating]]

#+BEGIN_SRC bash

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash

#+END_SRC