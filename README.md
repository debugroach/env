1.大致思路
用scoop安装编程环境， winget安装常用软件(用scoop安装软件容易出现奇奇怪怪的bug)， 代理clash。
2.常用软件（PowerShell下运行）
终端
winget install --name "windows terminal"
Google Chrome
winget install --id Google.Chrome
苹果音乐
winget install --name "Apple Music Preview"
VsCode
winget install --name "Microsoft Visual Studio Code"
PowerToys
winget install --name Microsoft PowerToys
3.编程环境（PowerShell下运行）
Aria2 （多线程下载工具）
scoop install aria2
Git （这里会安装7zip）
scoop install main/git
gcc
scoop install gcc
go
scoop install go       
go proxy
go env -w GO111MODULE=on
go env -w GOPROXY=https://goproxy.cn,direct
 字体JetBrains Mono
scoop bucket add nerd-fonts
scoop install nerd-fonts/JetBrains-Mono
scoop install nerd-fonts/JetBrainsMono-NF
4.终端配置
外观（dracula）

添加图片注释，不超过 140 字（可选）
settings.json文件中找到schemes部分 粘贴
    {
        "name": "Dracula",
        "cursorColor": "#F8F8F2",
        "selectionBackground": "#44475A",
        "background": "#282A36",
        "foreground": "#F8F8F2",
        "black": "#21222C",
        "blue": "#BD93F9",
        "cyan": "#8BE9FD",
        "green": "#50FA7B",
        "purple": "#FF79C6",
        "red": "#FF5555",
        "white": "#F8F8F2",
        "yellow": "#F1FA8C",
        "brightBlack": "#6272A4",
        "brightBlue": "#D6ACFF",
        "brightCyan": "#A4FFFF",
        "brightGreen": "#69FF94",
        "brightPurple": "#FF92DF",
        "brightRed": "#FF6E6E",
        "brightWhite": "#FFFFFF",
        "brightYellow": "#FFFFA5"
    }
配色方案选择Dracula
字体选择JetBrainsMono Nerd Font
5.oh my posh配置
安装oh my posh
winget install XP8K0HKJFRXGCK
更换主题
code $PROFILE
添加
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\powerlevel10k_rainbow.omp.json" | Invoke-Expression
重新打开终端

添加图片注释，不超过 140 字（可选）
待补充