## powershell指令示例
```
# 查询 CLOSE_WAIT状态 数量
Netstat -ano | findstr "CLOSE_WAIT" | Measure-Object -Line
# 文件中搜索关键字
Select-String "org.apache.catalina.startup.Catalina.start Server startup in" D:\tomcat\logs\catalina.2025-07-23.log
# 格式化输出时间
Get-Date -Format 'yyyy-MM-dd'
# 重命名文件
Rename-Item '.\2025 Jul GPLM System status.pptx' '2025 Aug GPLM System status.pptx'
```
