# ZSH

## vim mode

Install via `brew install zsh-vi-mode`

And add this to `~/.zshrc`

```zsh
source $(brew --prefix)/opt/zsh-vi-mode/share/zsh-vi-mode/zsh-vi-mode.plugin.zsh
```

## Basic functions

Helper zsh scripts to re-init the console

```zsh
function zsh-init() {
    source ~/.zshrc
}

function zsh-edit() {
    vi ~/.zshrc
}

function zsh-history() {
    history 0
}
```

## Other helpful functions

```zsh
function jq-less() {
    # Run the input json through jq, preserving color and without wrapping
    jq . --color-output | less -RS
}
```
