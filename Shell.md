# Shell

- ZSH Shell
- Powerlevels 10k: <https://github.com/romkatv/powerlevel10k>

# TMUX

tmux: <https://github.com/tmux/tmux/wiki>

tpm (plugin manager): <https://github.com/tmux-plugins/tpm>

## Plugins

- floax (floating scratch pane): <https://github.com/omerxx/tmux-floax> — requires tmux >= 3.3
  - `<prefix> + p` toggle floating pane, `<prefix> + P` menu (resize/move/full screen)
  - overrides the tmux default `<prefix> + p` (previous-window); use `M-H` / `M-L` for window navigation

## Installing plugins

After a fresh setup, start tmux and press `<prefix> + I` (Ctrl+Space, then Shift+i) to let tpm fetch the plugins.

# Ansible

- Script: [ansible-setup-shell.yml](./ansible-setup-shell.yml)

## Roles Structure

The configuration is organized into dedicated Ansible roles under `roles/`:
- **`common`**: OS compatibility check, locale generation, and base packages (`zsh`, `tmux`, `fzf`, `bat`, `neovim`, etc.).
- **`fonts`**: Meslo Nerd Fonts installation and font cache refresh.
- **`zsh`**: Zap plugin manager installation, `.zshrc` configuration template, and `.p10k.zsh` theme.
- **`tmux`**: Tmux Plugin Manager (`tpm`) installation and `.tmux.conf` configuration.

Global configuration defaults reside in `group_vars/all.yml`.

## Installation

- Python: `python3 -m pip install --user ansible`

## Running Playbook

- local System: `sudo -E ansible-playbook -i localhost, -c local ansible-setup-shell.yml`
- single Server: `ansible-playbook -i <ip_or_hostname>, -u <user> --ask-become-pass ansible-setup-shell.yml`

