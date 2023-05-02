#### 修改用户名导致git无法使用

解决办法：修改仓库的所有权

1. 使用管理员权限进入powershell

2. ```powershell
   icacls "file/path" /setowner YourUsername /t /c
   ```

批量修改脚本：

```powershell
$rootDir = "D:/Tech" # Git 仓库的根目录
$username = $env:UserName # 自动获取当前 Windows 用户名

Get-ChildItem -Path $rootDir -Recurse -Directory -Filter ".git" | ForEach-Object {
    $repoDir = $_.Parent.FullName
    Write-Host "Changing ownership of $repoDir to $username"
    icacls $repoDir /setowner $username /t /c
}
```

