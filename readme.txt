SSH kEYS���ɲ���
https://blog.csdn.net/u014704415/article/details/51605526

һ ������Git��user name��email��

$ git config --global user.name "xuhaiyan"
$ git config --global user.email "haiyan.xu.vip@gmail.com"

��������SSH��Կ���̣�
1.�鿴�Ƿ��Ѿ�����ssh��Կ��cd ~/.ssh
���û����Կ�򲻻��д��ļ��У����򱸷�ɾ��
2.������Կ��
$ ssh-keygen -t rsa -C ��haiyan.xu.vip@gmail.com��
��3���س�������Ϊ�ա�
���õ��������ļ���id_rsa��id_rsa.pub
3.�����Կ��ssh��ssh-add �ļ���
��Ҫ֮ǰ�������롣
4.��github�����ssh��Կ����Ҫ��ӵ��ǡ�id_rsa.pub������Ĺ�Կ��
5.���ԣ�ssh git@github.com
2����֤�Ƿ�ɹ�����git bash������
$ ssh -T git@github.com
�س��ͻῴ����You��ve successfully authenticated, but GitHub does not provide shell access ����ͱ�ʾ�ѳɹ�����github


ʹ��SSH����Git Զ�ֿ̲�ͱ��ؿ�����
https://blog.csdn.net/chenxi_li/article/details/93380649

ssh-keygen -t rsa �е�t��ʲô��˼��
https://blog.csdn.net/microcosmv/article/details/62054835
-t type
ָ��Ҫ��������Կ���͡�����ʹ�ã���rsa1��(SSH-1) ��rsa��(SSH-2) ��dsa��(SSH-2)
ssh-keygen -t rsa -C "ע�����ݣ�һ��Ϊ�ʼ���ַ"�����ɵĹ�Կ��������ע�ͣ�

���� Linuxƽ̨��ʹ��

cmder����������Կ��:
1.˽Կ
id_rsa

2.��Կ
id_rsa.pub

SSH��Կ����:
1.win������Կ��
ssh-keygen -t rsa

2.����.SSHĿ¼ 
cd C:\Users\Administrator\.ssh

3.�ѹ�Կ������linux��/root/.sshĿ¼��
scp id_rsa.pub root@192.168.2.1:/root/.ssh

4.��linux�ϰѹ�Կ����
mv id_rsa.pub authorized_keys

5.�ͻ����޿������-�������
ssh root@192.168.2.1

6.�ͻ����޿������-�ļ�����
scp index.php root@192.168.2.1:/root/