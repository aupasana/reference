# Things to Backup

Generate installed info:

  - brew -- `brew leaves --installed-on-request`
  - vscode -- `code --list-extensions --show-versions`

Config to backup:

  - books -- `~/Books`
  - config for various tools in `~/.config`
    - code -- `~/.config/vscode/*.code-workspace` 
    - nvim -- `~/.config/nvim/init.vim`
    - zsh -- `~/.config/zsh/*.zsh` and `~/.config/zsh/.zshrc`
  - scripts -- `~/src/scripts`
  - startup serivces -- `ls` in each of the following
    - `/System/Library/LaunchDaemons`, `/Library/LaunchDaemons`, `~/Library/LaunchDaemons`
    - `/System/Library/LaunchAgents`, `/Library/LaunchAgents`, `~/Library/LaunchAgents`

UX Config to backup:

  - chrome settings (search engines)
  - alfred preferences (search engines)
