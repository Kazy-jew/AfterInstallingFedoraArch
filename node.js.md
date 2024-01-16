# node.js 环境搭建


## 0.代理

国内网络依然是老大难的问题，记录一下备份

```
// 代理设置
npm config set proxy http://127.0.0.1:7890 -g
npm config set https-proxy http://127.0.0.1:7890 -g
npm set strict-ssl=false

//
查看下载进度, 以electron为例
npm install --verbose electron --save-dev
```


## 1.开始一项工程
