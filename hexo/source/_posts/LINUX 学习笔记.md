# LINUX 学习笔记

### yum 常用命令

```shell
# 列出所有仓库
yum repolist all
# 列出仓库所有软件包
yum list all
# 查看软件包信息
yum info 软件包名称
# 安装软件包
yum  install 软件包名称
# 升级软件包
yum update 软件包名称
# 移除软件包
yum remove 软件包
# 清除所有仓库缓存
yum clean all
# 查看可更新的软件包
yum check-update
# 查看系统中已经安装的软件包组
yum grouplist
# 安装指定的软件包组
yum groupinstall 软件包组
# 移除指定的软件包组
yum groupremove
# 查看指定的软件包组信息
yum groupinfo 软件包组

```

### history 命令

1.history命令用于显示历史执行过的命令

2.！编码数字     可以重复执行某一次的命令

3. 要清空当前用户在本机上执行的Linux命令历史记录信息，可执行如下命令

```shell
history -c
```

sosreport 命令

sosreport命令用于收集系统配置及架构信息并输出诊断文档，格式为sosreport



### 文本文件编辑命令

#### 查看文本

```shell
# 1.cat 查看内容较小的存文本文件
cat  -n  fileName  # -n  显示行号
# 2.more 用于查看纯文本文件（内容较多的）
more fileNmae 
# 3.head命令用于查看纯文本文档的前N行
head -n 20 filenNme
# 4.tail 令用于查看纯文本文档的后N行或持续刷新内容
tail -f  fileName

```

#### 文本操作

```shell
# 1.tr命令用于替换文本文件中的字符tr [原始字符] [目标字符]
cat fileName | tr [a-z] [A-Z]  #文本内容中的英文全部替换为大写
```

```shell
# 1.stat命令用于查看文件的具体存储信息和时间等信息
stat fileName
# 2cut命令用于按“列”提取文本字符，格式为“cut [参数]文本”
cut -d: -f1 fileName  # -d参数来设置间隔符号  -f 指定列
```

#### 文本比较

```shell
# 1.diff命令 
# diff --brief  命令显示比较后的结果，判断文件是否相同
diff -q fileName_A  fileName_B # -q 与 brief 等价
# 描述文件内容具体的不同
diff -c fileName_A  fileName_B 

```

### 文件目录管理

```shell
# 1.touch 命令 touch命令用于创建空白文件或设置文件的时间 touch [选项] [文件]
# 创建空白文件  linuxprobe
touch linuxprobe
# 修改文件的 读取及修改时间
touch -d "2019-05-05 14:00:00" linuxprobe
# 2.mkdir 命令 mkdir命令用于创建空白的目录
# 创建空白文件夹 linuxprobe
mkdir linuxprobe
# mkdir -p 创建有层级的文件夹
mkdir -p a/b/c

```

