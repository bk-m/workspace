## Download `Droid Sans Mono` if not present on system
> https://fonts.google.com/specimen/Droid+Sans+Mono
- install and make sure it works

## Download `CMDer` (with or w/o git)
> http://cmder.net/
```
set PATH=%ConEmuBaseDir%\Scripts;%PATH%
 
alias c=clear
alias ll=ls -la --color $*
alias ..=cd ..
alias ...=cd ..\..
alias ~=cd %USERPROFILE%
alias emacs=C:\Tools\emacs-25.2-x86_64\bin\emacs.exe --no-window-system $*
 
alias n=micro %USERPROFILE%\Dropbox\__NOTES__\$*.txt
alias nll=ls -la -c %USERPROFILE%\Dropbox\__NOTES__\
alias nls=ls -c %USERPROFILE%\Dropbox\__NOTES__\ | grep $*
alias ncd=cd %USERPROFILE%\Dropbox\__NOTES__\
 
alias pi=ssh pi@XX.XX.XX.XX
```
- set correct paths for `alias`'
- theme: `zenburn`
- `Settings -> Main`:
    - Font: `Droid Sans Mono`
    - Size: 16
- `Settings -> Keys & Macro`:
    - Make sure global hotkey `Ctrl+ö` is set to `Minimize/Restore (Quake-style)
- add `path`s to: `%CMDER_ROOT%\config\user-profile.cmd`

## Download `micro`
> https://micro-editor.github.io/
- place `micro.exe` in `%CMDER_ROOT%/bin`

## Download `Git` for Windows (if not downloaded with `cmder`)
> https://git-scm.com/download
```sh
$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
$ git config --global core.editor emacs
```
- make sure `GitFlow` works
- add to `path` of not done by setup

## Download `Emacs`
> https://www.gnu.org/software/emacs/
- add to `cmder's path`
- setup `cmder alias` for emacs

## Download `AutoHotkey`
> https://autohotkey.com/

Basic script to map `Capslock` to `CTRL`
```autohotkey
#NoEnv  ; Recommended for performance and compatibility with future AutoHotkey releases.
; #Warn  ; Enable warnings to assist with detecting common errors.
SendMode Input  ; Recommended for new scripts due to its superior speed and reliability.
SetWorkingDir %A_ScriptDir%  ; Ensures a consistent starting directory.
Capslock::Ctrl
```

Variation of previous script that only runs if no window with `XUbuntu` in the title is active
```autohotkey
#NoEnv  ; Recommended for performance and compatibility with future AutoHotkey releases.
; #Warn  ; Enable warnings to assist with detecting common errors.
SendMode Input  ; Recommended for new scripts due to its superior speed and reliability.
SetWorkingDir %A_ScriptDir%  ; Ensures a consistent starting directory.
SetTitleMatchMode 2
#IfWinNotActive, XUbuntu
Capslock::Ctrl
#IfWinNotActive
```
- compile `exe` and run

## Download `Anaconda3`
> https://www.anaconda.com/download/
- make sure all `path` vars are correctly set (in user vars)

![Anaconda Path](https://github.com/bk-m/workspace/blob/master/anaconda_path.PNG)

## Download `VS Code`
> https://code.visualstudio.com/

![VS Code extensions](https://github.com/bk-m/workspace/blob/master/vscode_extensions.PNG)

```json
// Place your settings in this file to overwrite the default settings
{
    "editor.fontFamily": "Droid Sans Mono",
    "editor.fontSize": 14,
    "editor.cursorBlinking": "solid",
    "editor.cursorStyle": "block",
    "telemetry.enableTelemetry": false,
    "telemetry.enableCrashReporter": false,
    "code-runner.runInTerminal": false,
    "startanyshell.shells": [
        {
            "description": "Cmder",
            "command": "C:\\Tools\\cmder\\Cmder.exe /start \"%path%\""
        },
        {
            "description": "Windows Command Prompt",
            "command": "start \"%description%\" /WAIT %comspec%"
        },
        {
            "description": "Git Bash 2",
            "command": "\"C:\\Program Files\\Git\\git-bash.exe\" \"--cd=%path%\""
        },
        {
            "description": "Windows Powershell",
            "command": "start \"%description%\" powershell.exe -noexit"
        }
    ],
"files.autoSave": "off",
"workbench.activityBar.visible": true,
"editor.rulers": [80, 100],
"markdown-pdf.type": "pdf",
"markdown-toc.withLinks": true,
"markdown-toc.orderedList": false,
"markdown-toc.depthFrom": 2,
"editor.renderIndentGuides": true,
"editor.insertSpaces": true,
"workbench.colorTheme": "Zenburn",
"workbench.iconTheme": "vscode-icons",
"editor.minimap.enabled": true,
"window.zoomLevel": 0,
"workbench.welcome.enabled": false,
"projectManager.vscode.baseFolders": [
    "%USERPROFILE%",
    "%USERPROFILE%\\Dropbox",
    "C:\\Users\\XXX\\Dropbox\\code"
],
"projectManager.git.baseFolders": [
    "%USERPROFILE%",
    "%USERPROFILE%\\Dropbox",
    "C:\\Users\\XXX\\Dropbox\\code"]
}
```
- in `Settings` file set correct paths for:
    - `Cmder`
    - `git-bash`
    - `Project Manager` plugin
- add `<vscode_root>\bin` to `cmder's path var`

## Optional Tools
- Notepad++
- Slack
- Discord
- Spotify
- Dropbox
- pgAdmin / phpMyAdmin / SQLite Database Browser
- WinSCP
- KeePass2
- SourceTree (or some other Git GUI)