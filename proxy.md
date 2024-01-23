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

环境变量里配置<font style="color:red">⸸</font>
```
HTTPS_PROXY=http://127.0.0.1:7890
HTTP_PROXY=http://127.0.0.1:7890
NO_PROXY=127.0.0.1,localhost
```
<font style="color:red">⸸</font><font size=2>1.`HTTP_PROXY` & `HTTPS_PROXY`代理协议都设为http是因为代理软件不支持https;<br />&nbsp;&nbsp;2.`NO_PROXY`是为了访问本地地址时绕过代理，没有这个值会导致一些程序的访问出现问题，具体如cmd中用curl调用本地起的服务的api调用不到，以及前端框架angular/react页面在浏览器中打不开等等</font>

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