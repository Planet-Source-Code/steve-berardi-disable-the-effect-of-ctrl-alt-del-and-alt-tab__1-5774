<div align="center">

## Disable the effect of Ctrl\+Alt\+Del and Alt\+Tab


</div>

### Description

Disables the effect of Ctrl+Alt+Del and Alt-Tab. It can be used for security programs or just so the user cant exit your program or restart the computer from the keyboard.
 
### More Info
 
This code accomplishes it's task by telling Windows that a screen saver is running, therefor, ctrl+alt+del wont work.

Note that this code disables the use of restarting your computer by hitting ctrl+alt+del. The only way the user will be able to restart the computer would be to turn it off then back on. I also included the code to enable ctrl+alt+del again.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Steve Berardi](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/steve-berardi.md)
**Level**          |Intermediate
**User Rating**    |4.8 (177 globes from 37 users)
**Compatibility**  |VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__1-1.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/steve-berardi-disable-the-effect-of-ctrl-alt-del-and-alt-tab__1-5774/archive/master.zip)

### API Declarations

```
Private Declare Function SystemParametersInfo Lib "user32" Alias "SystemParametersInfoA" (ByVal uAction As Long, ByVal uParam As Long, lpvParam As Any, ByVal fuWinIni As Long) As Long
Private Const SPI_SCREENSAVERRUNNING = 97
```


### Source Code

```
Sub Enable_TaskView()
 Dim eTask As Integer
 Dim junk As Boolean
 eTask = SystemParametersInfo(SPI_SCREENSAVERRUNNING, False, junk, 0)
End Sub
Sub Disable_TaskView()
 Dim dTask As Integer
 Dim junk As Boolean
 dTask = SystemParametersInfo(SPI_SCREENSAVERRUNNING, True, junk, 0)
End Sub
```

