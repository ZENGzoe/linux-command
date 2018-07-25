# 命令行汇总

##Linux

**查看当前路径**

```bash
pwd
```

**创建文件夹**

```bash
mkdir dirName
```

**创建文件**

```bash
touch fileName
//创建xx路径下
touch xx/fileName
```

**变更文件的拥有者**

```bash
chown -R 变更后的拥有者: fileName/dirName
```

---

##vim

**退出vim**

正常模式：

按住`shift`

`zz` 保存退出
`zq` 不保存退出

命令编辑模式：

先按`esc` 

`:q` 不保存退出
`:q!` 不保存强制退出
`:wq` 保存退出，无论是否修改，都会修改时间戳
`:x`  保存退出，如果未修改内容，则不会修改时间戳

**切换到编辑模式**

在正常模式下按下`i` `I` `a` `A`等健

---

##Git

**查看远程分支**

```bash
git branch -a
```

**切换到远程分支**

如远程分支有`remotes/origin/xxx`

```bash
git branch origin/xxx -b xxx
```

##npm

**使用淘宝镜像**

```bash
npm install -g cnpm --registry=https://registry.npm.taobao.org
```
