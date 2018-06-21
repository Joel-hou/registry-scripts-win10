# Better Use Windows 10 

## Software to enhance your experience with Windows 10
### Tool
- Chrome
- Office
- CloudMusic
- Shadowsocks
- Vmware
- CCleaner
- Free Download Manager
- Winrar

Create a new file named rarreg.key contains the following lines 
```
RAR registration data
yaokai.com
Unlimited Company License
UID=636da5a1e3718a4597b9
641221225097b94b94094a6548ed8365940161a87853d63b09c6ff
0b86c572d75fb683db5960fce6cb5ffde62890079861be57638717
7131ced835ed65cc743d9777f2ea71a8e32c7e593cf66794343565
b41bcf56929486b8bcdac33d50ecf77399608cfb51a0f9e15e798c
57fc8a5e5c3fc69a04ae7d4ec41408c506ff1c90962e165207a4e9
45d426eae53d8849d222b3b26997e5e18b4526596c75d682603e01
1364c589ec5fcea9fa5b796e3fa7437cd080392e5d791757768079
```
Placed it under the directory where winrar is installed
- Dism++
- Eudic
- Listary
  选项->关键字->Web 添加 "Keyeyword: zh" "Display title: Search Zhihu for {query}" URL: 
  ```
  https://www.zhihu.com/search?type=content&q={query}
  ```
  选项->关键字->Web 添加 "Keyeyword: gh" "Display title: Search Github for {query}" URL: 
  ```
  https://github.com/search?q={query} 
  ```

### Social
- Tim
- WeChat
### Coder
- Git
```
git config --global user.name "youName"
git config --global user.email "youremail@example.com"

git config --global color.status auto
git config --global color.diff auto  
git config --global color.branch auto 
git config --global color.interactive true
git config --global core.pager "less -x1,5"
git config --global push.default simple 
git config --global pull.ff only  
git config --global merge.ff only  
```
- VScode
  
  Plugins:
  - Vim
  - Code Runner
  - Verdandi Theme

- JDK, Python
- Idea/Webstorm/pyCharm
- Vim/Neovim
- Settings -> Update&Security -> For Developers -> Developer Mode
### UWP apps
- Wunderlist
- iTunes

## Make cmd look better
1. Install fonts

    You can download fonts from  https://be5invis.github.io/Iosevka/inziu.html 

    Don't forget to import true-type-cmd-font.reg to your registery
2. Import cmd color
    https://github.com/Microsoft/console/tree/master/tools/ColorTool
    ```
    colortool -b campbell
    ```
    Don't forget to save your cmd Properties after color imported

## Beautify powershell
Note: You should be administrator account and set execution policy 
```
Set-ExecutionPolicy -Scope CurrentUser Bypass
```
1. Install necessary modules 
```
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
Install-Module PSColor -Scope CurrentUser
Install-Module DirColors -Scope CurrentUser
```
Display system info if you like, it looks good but useless
```
Install-Module windows-screenfetch -Scope CurrentUser
```
2. Create your powershell configuration file

  "Microsoft.PowerShell_profile.ps1" located in ~/Documents, you can see by typing $profile in powershell windows, add following lines according to your needs
```
Import-Module DirColors
Import-Module PSColor
Update-DirColors D:\your_user_name\Documents\WindowsPowerShell\dircolors\dircolors.ansi-dark

Import-Module posh-git
Import-Module oh-my-posh

if (!(Get-SshAgent)) {
    Start-SshAgent
}

Set-Theme PowerLine
# Screenfetch
```
## Here are some other tips to make Windows easier to use 
- Change Capslock to Esc

  Just right click capslock-to-esc.reg
- Make your taskbar transparent (before win10 version 1803)

  Just right click transparent-taskbar to import entries
- Add "Edit with Vim" to right click menu

  Right click add-edit-with-neovim.reg
- Automatically empty the recycle bin after you log in

  Task Scheduler create new task
```
cmd.exe /c "echo Y|PowerShell.exe -NoProfile -Command Clear-RecycleBin"
```
