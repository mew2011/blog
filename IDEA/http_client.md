## Http Client环境设置
编辑http-client.env.json文件
```json
{
  "local": {
    "host": "http://localhost:8080/"
  },
  "dev": {
    "host": "https://xxx.abc.com/"
  },
  "qas": {
    "host": "https://xxx.sss.com/"
  },
  "prd": {
    "host": "https://xxx.aaa.com/"
  }
}
```

## GET请求
```
GET http://127.0.0.1:8080/user/one
```

## POST请求
```
POST http://127.0.0.1:8080/user
Content-Type: application/json

{
  "name": "Alice"
}
```

## 文件上传
```
###
POST http://localhost:8088/abc/importFile
Cache-Control: no-cache
Content-Type: multipart/form-data; boundary=WebAppBoundary

--WebAppBoundary
Content-Disposition: form-data; name="file"; filename="abc.xlsx"
Content-Type: multipart/form-data

< D:\IMPORT\abc.xlsx
--WebAppBoundary--
```
