# dotfiles

This repo contains the configuration to setup my machines. This is using [Chezmoi](https://chezmoi.io), the dotfile manager to setup the install.

This automated setup is currently tested on ubuntu machines.

## How to run

```shell
export GITHUB_USERNAME=andreas-pal
sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply $GITHUB_USERNAME
```
## How to run on VM 2025 ##
```shell
sudo snap install chezmoi --classic
sudo snap install curl
sudo apt install git -y
ssh-keyscan github.com >> ~/.ssh/known_hosts
chezmoi init git@github.com:andreas-pal/dotfiles.git
chezmoi apply
```
