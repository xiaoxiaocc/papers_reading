## git初始化建库以及与远程github仓库建立联系

### ssh相关配置

1. 本地生成ssh 公钥和密钥

```shell
$ ssh-keygen -t rsa -P '' -f ~/.ssh/id_rsa

ssh-keygen是用于生产密钥的工具。

-t：指定生成密钥类型（rsa、dsa、ecdsa等）
-P：指定passphrase，用于确保私钥的安全
-f：指定存放密钥的文件（公钥文件默认和私钥同目录下，不同的是，存放公钥的文件名需要加上后缀.pub

id_rsa：保存私钥
id_rsa.pub：保存公钥
known_hosts：保存已认证的远程主机ID（关于known_hosts详情，见文末更新内容）
```

2. 将公钥在粘贴到https://github.com/settings/keys

### 本地仓库关联github仓库

1. github上新建一个仓库
2. 本地要建立仓库的地方: git init
3. git remote add origin git@github.com:xiaoxiaocc/papers_reading.git  这部分内容来自github新建的仓库
4. git branch --set-upstream-to origin/master
5. git pull --rebase
6. git push


