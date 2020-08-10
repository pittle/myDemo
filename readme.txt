SSH kEYS生成步骤
https://blog.csdn.net/u014704415/article/details/51605526

一 、设置Git的user name和email：

$ git config --global user.name "xuhaiyan"
$ git config --global user.email "haiyan.xu.vip@gmail.com"

二、生成SSH密钥过程：
1.查看是否已经有了ssh密钥：cd ~/.ssh
如果没有密钥则不会有此文件夹，有则备份删除
2.生存密钥：
$ ssh-keygen -t rsa -C “haiyan.xu.vip@gmail.com”
按3个回车，密码为空。
最后得到了两个文件：id_rsa和id_rsa.pub
3.添加密钥到ssh：ssh-add 文件名
需要之前输入密码。
4.在github上添加ssh密钥，这要添加的是“id_rsa.pub”里面的公钥。
5.测试：ssh git@github.com
2）验证是否成功，在git bash下输入
$ ssh -T git@github.com
回车就会看到：You’ve successfully authenticated, but GitHub does not provide shell access 。这就表示已成功连上github


使用SSH建立Git 远程仓库和本地库连接
https://blog.csdn.net/chenxi_li/article/details/93380649

ssh-keygen -t rsa 中的t是什么意思？
https://blog.csdn.net/microcosmv/article/details/62054835
-t type
指定要创建的密钥类型。可以使用：”rsa1”(SSH-1) “rsa”(SSH-2) “dsa”(SSH-2)
ssh-keygen -t rsa -C "注释内容，一般为邮件地址"，生成的公钥后面会带上注释，

三： Linux平台上使用

cmder可以生成密钥对:
1.私钥
id_rsa

2.公钥
id_rsa.pub

SSH密钥操作:
1.win生成密钥对
ssh-keygen -t rsa

2.进入.SSH目录 
cd C:\Users\Administrator\.ssh

3.把公钥拷贝到linux下/root/.ssh目录下
scp id_rsa.pub root@192.168.2.1:/root/.ssh

4.在linux上把公钥改名
mv id_rsa.pub authorized_keys

5.客户端无口令测试-命令操作
ssh root@192.168.2.1

6.客户端无口令测试-文件传输
scp index.php root@192.168.2.1:/root/