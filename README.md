Fallowing are the steps for user service in Todoapp

#apt update

#mkdir home

#cd /root/home/

#git clone https://github.com/zelar-soft-todoapp/users.git

#cd users/

#apt update

#apt install openjdk-8-jdkpdate

#java -version

#apt install maven -y

#mvn package

#cd target

#vi /etc/systemd/system/users.service

#systemctl daemon-reload

#systemctl start users

#systemctl enable users

#systemctl status users
