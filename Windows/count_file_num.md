你可以使用 PowerShell 来递归统计当前目录（及其子目录）下所有 .java 文件的数量。以下是常用的一行命令：

```powershell
Get-ChildItem -Recurse -Filter *.java | Measure-Object | Select-Object -ExpandProperty Count
```

**解释：**

- `Get-ChildItem -Recurse -Filter *.java`：递归查找所有 .java 文件。
- `Measure-Object`：统计对象数量。
- `Select-Object -ExpandProperty Count`：只输出统计数值。

如果要统计某个指定路径下的 .java 文件数量，例如 `src` 目录：

```powershell
Get-ChildItem -Path .\src -Recurse -Filter *.java | Measure-Object | Select-Object -ExpandProperty Count
```

如果你还需要统计所有文件的详细路径，也可以这样：

```powershell
Get-ChildItem -Recurse -Filter *.java | Select-Object FullName
```

如需其他统计方式，可补充需求！
