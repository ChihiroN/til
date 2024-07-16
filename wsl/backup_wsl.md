wslでは構築済みの環境をバックアップ・インポートすることができる

# tar エクスポート
```
wsl --export Ubuntu  c:\tmp\ubuntu.tar
```
# tar インポート
```
wsl --import My-Ubuntu c:\wsl\My-Ubuntu\ c:\Download\ubuntu.tar
```
# ユーザ名を変更
```
wsl -u root -d Ubuntu
```
```
usermod -l 変更後のユーザ名 変更前のユーザ名
groupmod -n 変更後のユーザ名 変更前のユーザ名
usermod -d /home/変更後のユーザ名 -m 変更後のユーザ名
exit
```

# Powershellでデフォルトユーザを変更
```
Function WSL-SetDefaultUser ($distro, $user) { Get-ItemProperty Registry::HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Lxss\*\ DistributionName | Where-Object -Property DistributionName -eq $distro | Set-ItemProperty -Name DefaultUid -Value ((wsl -d $distro -u $user -e id -u) | Out-String); };
```
# 実行
```
WSL-SetDefaultUser Ubuntu ユーザ名
exit
```
