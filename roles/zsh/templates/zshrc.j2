# OS Family set by Ansible
export OS_FAMILY="{{ ansible_facts['os_family'] }}"

# Enable Powerlevel10k instant prompt. Must stay at the top.
if [[ -r "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh" ]]; then
  source "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh"
fi

# Set default locale settings
export LANG="en_US.UTF-8"       # For English messages and general defaults
export LC_TIME="de_DE.UTF-8"    # For German date and time formats
export LC_NUMERIC="de_DE.UTF-8" # For German number formats (decimal comma, thousands dot)
export LC_COLLATE="de_DE.UTF-8" # For German sorting rules (e.g., ä sorts with a)

# History configuration
HISTFILE=~/.zsh_history
HISTSIZE=100000
SAVEHIST=100000

# Share history between all sessions (including tmux panes/windows)
setopt SHARE_HISTORY

setopt INC_APPEND_HISTORY
setopt HIST_IGNORE_DUPS
setopt HIST_IGNORE_SPACE
setopt HIST_FCNTL_LOCK


# Zap
[ -f "${XDG_DATA_HOME:-$HOME/.local/share}/zap/zap.zsh" ] && source "${XDG_DATA_HOME:-$HOME/.local/share}/zap/zap.zsh"

fpath=(~/.zsh/completions /usr/share/zsh/vendor-completions $fpath)

if (( $+commands[just] )); then
  if [[ ! -f ~/.zsh/completions/_just || ~/.zsh/completions/_just -ot $commands[just] ]]; then
    mkdir -p ~/.zsh/completions
    just --completions zsh > ~/.zsh/completions/_just
  fi
fi

# Initialize the completion system
autoload -Uz compinit
compinit
# Make Autocompletion Case Insensitive
zstyle ':completion:*' matcher-list 'm:{a-z}={A-Z}'

# Plugins
plug "romkatv/powerlevel10k"
plug "chivalryq/git-alias"
plug "zsh-users/zsh-syntax-highlighting"
plug "MichaelAquilina/zsh-you-should-use"
plug "zsh-users/zsh-completions"
plug "zsh-users/zsh-autosuggestions" # Ghost Guesser
plug "Aloxaf/fzf-tab"                # fzf-powered tab completion

# Editor
export EDITOR=nvim
export VISUAL=nvim

# Aliases
alias lg='lazygit'
alias open='xdg-open'

## Directories
setopt auto_cd
setopt auto_pushd
setopt pushd_ignore_dups
setopt pushdminus

alias -g ...='../..'
alias -g ....='../../..'
alias -g .....='../../../..'
alias -g ......='../../../../..'

alias -- -='cd -'
alias 1='cd -1'
alias 2='cd -2'
alias 3='cd -3'
alias 4='cd -4'
alias 5='cd -5'
alias 6='cd -6'
alias 7='cd -7'
alias 8='cd -8'
alias 9='cd -9'

alias md='mkdir -p'
alias rd=rmdir

alias la='ls -a'
alias lla='ls -la'

alias devc-start='devcontainer up --workspace-folder .'
alias devc-cli='devcontainer exec --workspace-folder . bash'

# On Ubuntu Only
if [[ "$OS_FAMILY" == "Debian" ]]; then
  source /usr/share/doc/fzf/examples/key-bindings.zsh
fi

# FZF
export FZF_CTRL_T_OPTS="--preview '
  if [ -d {} ]; then
    ls -la {}
  elif file {} | grep -q text; then
    bat --color=always {}
  else
    echo \"binary file\"
  fi
' --preview-window 'right:60%:wrap'"

source <(fzf --zsh)

# Map Up arrow to fzf history search
bindkey '^[[A' fzf-history-widget
bindkey '^[OA' fzf-history-widget

# Powerlevel10k config
[[ ! -f ~/.p10k.zsh ]] || source ~/.p10k.zsh
