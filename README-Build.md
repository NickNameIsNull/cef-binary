# 如何使用
在当前目录运行 build.ps1



## # build.ps1参数

| 参数            | 含义                                        | 值域                                      | 示例                                                         |
| --------------- | ------------------------------------------- | ----------------------------------------- | ------------------------------------------------------------ |
| Target          | 指定脚本编译目标                            | "vs2019", "vs2022", "nupkg", "nupkg-only" |                                                              |
| DownloadBinary  | 下载Cef二进制行为                           | "none", "download", "local"               |                                                              |
| CefBinaryDir    | 包含cef二进制文件存档的目录的绝对或相对路径 | 在DownloadBinary = local时使用            | /cefsource/                                                  |
| Extension       | DownloadBinary 下载的文件扩展名             | "tar.bz2","zip","7z"                      |                                                              |
| BuildArches     | 构建平台架构                                |                                           | win-x86;win-x64;win-arm64                                    |
| SevenZipExePath | 7zip解压程序路径                            |                                           | C:\Program Files\7-Zip\7z.exe<br />C:\\Software\\Common\\7-Zip\\7z.exe |
| Suffix          | 版本后缀                                    |                                           | 为 "" 或 $null 或 0 z则不添加                                |
|                 |                                             |                                           |                                                              |

# 本地二进制编译调用

```powershell
.\build.ps1 -Target "nupkg" -DownloadBinary "local" -CefBinaryDir "../cef-binary-source/" -Extension "zip" -CefVersion "134.3.60+gfe66d80+chromium-134.0.6998.166" -SevenZipExePath "C:\\Software\\Common\\7-Zip\\7z.exe" -Suffix ""
```

