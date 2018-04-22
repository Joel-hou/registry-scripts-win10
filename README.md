# Better Use Windows 

## Software to enhance your experience with Windows 
- Listary
- Free Download Manager
- Git
- Vim/Neovim

## Make powershell better
1. Install oh-my-posh
```
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
```
Note: You should be administrator account and set execution policy unrestricted before via
```
Set-ExecutionPolicy Unrestricted
```
Create your powershell configuration file, you can see by typing $profile in powershell command windows, add following lines to make oh-my-posh work
```
Import-Module oh-my-posh
```
2. Install fonts
```
git clone git@github.com:powerline/fonts.git
cd fonts
# right click install.ps1 run with powershell 
```
3. Set theme
Last step, type "Set-Theme" space and tab to choose your theme

## Here are some other tips to make Windows easier to use 
- Change Capslock to Esc

  Just right click capslock-to-esc.reg
- Make your taskbar transparent

  Just right click transparent-taskbar to import entries
- Add "Edit with Vim" to right click menu

  Right click add-edit-with-neovim.reg
- Automatically empty the recycle bin after you logged in

  Task Scheduler create new task
```
cmd.exe /c "echo Y|PowerShell.exe -NoProfile -Command Clear-RecycleBin"
```
