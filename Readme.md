## Cmder Config

In my config, I mainly use powershell and install some modules. If you want to use this config for your cmder, please install the modules below.

1. First you should install PsGet:
  `(new-object Net.WebClient).DownloadString("http://psget.net/GetPsGet.ps1") | iex
Install-Module PowerLS`

2. Then you can install modules by using `Install-Module`
  - `Install-Module Jump.Location`
  > Use `j` to jump into folders just like autojump in linux
  >
  > e.g. `cd ~/.atom` after you enter that directory, you can simply use `j atom` enter into `~/.atom`. Just type `j` and return you can enter into the most common used directory. Cool!
  - `Install-Module Posh-git`
  > For git user
  - `Install-Module PSColor`
  > For highlighting
  - `Install-Module TabExpansionPlusPlus`
  > For using `Tab` completions

For Windows 10 users, you can use `alt+shift+3` into `Bash on ubuntu for windows`. There may be some problems in it, because I set the default shell is `ZSH`.

You can simply use `sh -c "$(curl -fsSL https://raw.githubusercontent.com/wayneg123/linux_configuration/master/zsh_theme.sh)"` to install ZSH from my [linux_configuration repo](https://github.com/wayneg123/linux_configuration).


All config files must be in this folder. If there is no option to set this folder
directly, it has to be hardlinked.

* `aliases`: aliases in cmd; called form vendor\init.bat; autocreated from
  `vendor\aliases.example`.
* `*.lua`: clink completions and prompt filters; called from vendor\cmder.lua after all
  other prompt filter and clink completions are initialized; add your own.
* `user_profile.{sh|bat|ps1}`: startup files for bash|cmd|powershell tasks; called from their
  respective startup scripts in `vendor\`; autocreated on first start of such a task
* `.history`: the current commandline history; autoupdated on close
* `settings`: settings for readline; overwritten on update
* `ConEmu.xml`: settings from ConEmu (=the UI of cmder -> Preferences); overwritten on update
