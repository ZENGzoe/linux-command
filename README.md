# 命令行汇总

## Linux

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

**查看端口**

```bash
lsof -i tcp:端口
```

**kill进程**

```bash
kill 进程PID
```

---

## vim

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

## Git

**查看远程分支**

```bash
git branch -a
```

**切换到远程分支**

如远程分支有`remotes/origin/xxx`

```bash
git branch origin/xxx -b xxx
```

**删掉远程仓库**

```bash
git remote rm origin
```

**添加远程仓库**

```bash
git remote add origin git地址
```

**查看远程仓库**

```bash
git remote -v
```

**合并分支**

如讲dev的代码合并到master：
```
git merge dev
```

**生成ssh公钥**

```
cd ~/.ssh
ssh-keygen
```

**删除submodule**

```
# 
git submodule deinit 子模块名
# 删除.gitmodules中记录的模块信息（--cached选项清除.git/modules中的缓存）
git rm --cached 子模块名
# 提交记录
git add .

```

## npm

**使用淘宝镜像**

```bash
npm install -g cnpm --registry=https://registry.npm.taobao.org
```

## mysql

**登陆*

```bash
mysql -uroot -p
//输入密码
```

**退出**

```
exit
```

**查看版本号**

```
mysql>status
```

### 数据库操作

**创建数据库**

```
create database 数据库名称;
```

**查看数据库**

```
show database;
```

**删除数据库**

```
drop database 数据库名称;
```

**打开数据库**

```
use 数据库名称;
```

### 数据表操作

**显示某个数据库中所有表**

```
show tables;
```

**显示数据表的结构**

```
desc 表名;
```

### 创建后表的修改

**修改列**

```
alter table 表名 change 列名称 新列名称 新数据类型;

//eg:

alter table book_lists change author author varchar(45) not null;

```

**添加新列**

```
alter table 表名 add 列名称 数据类型;

//eg:

alter table users add nickName varchar(50) not null;
```

### 数据操作

**查询数据**

```
select * from 表名 where 字段=值;
//or
select 列名 from 表名 where 字段=值;
```

**删除数据**

```
delete from 表名 where 字段=值;
```

**更新数据**

如果没有该数据，insert新数据，如果有，则更新数据。

```
replace into 表名 set 字段=值，字段=值...(字段中需有唯一的属性);
```





