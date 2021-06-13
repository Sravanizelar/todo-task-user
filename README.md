Fallowing are the steps for user service in Todoapp

#apt update

#useradd -m -s /bin/bash app

#cd /home/app/

#git clone https://github.com/zelar-soft-todoapp/users.git

#apt update

#apt install openjdk-8-jre-headless

#apt install openjdk-8-jdk-headless

#export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64

#apt install maven -y

#cd /home/app/users/

#mvn clean package
   
#cd target/

#java -jar users-api-0.0.1.jar

#vim /etc/systemd/service/users.service

#systemctl daemon-reload

#systemctl start users

#systemctl enable users

#systemctl ststus users


---------------------###############----------------
systemD File for users.service

systemd files ===  user.service files
   
[Unit]
Description=users service

[Service]
User=app
Environment=AUTH_API_PORT=REDIS_ENDPOINT
ExecStart=/bin/java -jar /home/app/users/target/users-api-0.0.1.jar
SyslogIdentifier=users

[Install]
WantedBy=multi-user.target
