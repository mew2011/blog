## node安装
```text
环境变量设置:
NODE_HOME=安装目录
path:
%NODE_HOME%
%NODE_HOME%\node_global
%NODE_HOME%\node_cache
```

```text
node安装目录新增目录:
node_global
node_cache

shell执行命令:
npm config set prefix "D:\apps\nodejs\node_global"
npm config set cache "D:\apps\nodejs\node_cache"
```
## npm全局和本地区别
```
全局安装的包秩序安装一次,之后在任何位置都可以使用这个包
本地安装的包,只能在当前目录下使用
```
## npm命令
全局安装
```
npm install -g express
```
查看全局包清单
```
npm list -g
```
本地安装
```
npm install express
```
