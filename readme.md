$realUser = (Get-WmiObject Win32_ComputerSystem).UserName.Split('\')[-1]
icacls "C:\Users\$realUser\.vscode\extensions" /remove:d $realUser
