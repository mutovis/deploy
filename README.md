# deploy

This repo contains [Ansible](https://www.ansible.com/) files used to configure and install [Mutovis](https://mutovis.com) software. Currently only Arch Linux based distros are supported ([Antergos](https://antergos.com/) and [the like](https://wiki.archlinux.org/index.php/Arch-based_distributions) *should* be okay).

## Usage Instructions
Run the following two lines as a user with sudo powers to install and setup Mutovis software:

```bash
sudo pacman -Syu ansible --needed
ansible-pull -U https://github.com/mutovis/deploy --ask-become-pass
```
for a successful installation, the `ansible-pull` command will end with a message similar to
```
PLAY RECAP ****************************************************************
127.0.0.1                  : ok=23   changed=8    unreachable=0    failed=0 
```
the `ok` and `changed` numbers above might be different, but the `unreachable` and `failed` numbers should both be zero.
For the first run, this may take several minutes to complete since several bits of software will be compiled here.  
Re-plug any USB <---> GPIB adapters after the installation is complete.
