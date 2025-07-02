## 端口占用处理
1. CMD窗口输入
```
netstat -aon | findstr "3000"
```
```
# 输出示例：
TCP    172.20.8.18:53000      142.250.69.170:443     SYN_SENT        29756
TCP    [::1]:3000             [::]:0                 LISTENING       11980
```

2. 根据PID查找对应的进程名称
```
tasklist | findstr "11980"
```
```
# 输出示例：
node.exe                  11980 Console                   15     21,688 K
```
3. 强制结束该进程
```
taskkill /PID 11980 /F
```
