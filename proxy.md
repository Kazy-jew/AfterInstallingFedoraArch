# 代理问题

最近要出国了，用不上代理了，把一些代理设置记录一下，
不然忘了出问题还要定位半天。。。

设置了代理的程序：

node,pip,git
pip 获取的是系统环境变量，node和git为单独设置

## 设置代理

### 1.系统环境变量

#### linux

.bashrc里配置

#### windows

环境变量里配置

### 2.git

```
git config --global http.proxy http://127.0.0.1:7890
git config --global https.proxy http://127.0.0.1:7890
```

### 3.npm

```
npm config set proxy http://127.0.0.1:7890 -g
npm config set https-proxy http://127.0.0.1:7890 -g
npm set strict-ssl=false
```


## 删除代理

### 1.系统环境变量

#### linux

.bashrc里注释掉配置即可

#### windows

系统环境变量删除环境变量里的HTTP_PROXY和HTTPS_PROXY即可


### 2.git

```
git config --global --unset http.proxy
git config --global --unset http.proxy
```

### 3.npm

```
```