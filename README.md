# deploy

This repo contains [Ansible](https://www.ansible.com/) files used to configure and install [Mutovis](https://mutovis.com) software. Currently only Arch Linux based distros are supported ([Antergos](https://antergos.com/) and [the like](https://wiki.archlinux.org/index.php/Arch-based_distributions) *should* be okay).

## Usage Instructions
Run the following as a user with sudo powers to install and setup Mutovis software:

```bash
sudo pacman -Syu ansible --needed
ansible-pull -U https://github.com/mutovis/deploy --ask-become-pass
```
