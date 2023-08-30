方法1

sudo -i切换到root

passwd设置密码

sudo sed -i 's/^#\?PermitRootLogin.*/PermitRootLogin yes/g' /etc/ssh/sshd_config;

sudo sed -i 's/^#\?PasswordAuthentication.*/PasswordAuthentication yes/g' /etc/ssh/sshd_config;

sudo service sshd restart

reboot重启服务器


方法2
sudo -i  用root身份

passwd  设置root密码

vi /etc/ssh/sshd_config   修改配置文件

PermitRootLogin yes

PasswordAuthentication yes

reboot重启服务器
