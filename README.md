# node-todo-cicd

Run these commands:


`sudo apt install nodejs`


`sudo apt install npm`


`npm install`

`node app.js`



# Live DevOps Project for Resume - Jenkins CICD with GitHub Integration (Notes)

1)	Create AWS EC2 instance
2)	sudo apt update
3)	    3  sudo apt install openjdk-11-jre
4)	    4  java -version
5)	    5  curl -fsSL https://pkg.jenkins.io/debian/jenkins.io.key | sudo tee \   /usr/share/keyrings/jenkins-keyring.asc > /dev/null 
6)	    6  echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \   https://pkg.jenkins.io/debian binary/ | sudo tee \   /etc/apt/sources.list.d/jenkins.list > /dev/null
7)	    7  sudo apt-get update 
8)	    8  sudo apt-get install jenkins
9)	    9  sudo systemctl enable jenkins
10)	   10  sudo systemctl start jenkins
11)	   11  sudo systemctl status jenkins
12)	   12  sudo cat /var/lib/jenkins/secrets/initialAdminPassword
13)	   13  sudo nano /etc/default/jenkins 
14)	   14  add JENKINS_LISTEN_ADDRESS="0.0.0.0" in the file
15)	sudo apt install docker.io
16)	FROM node:12.2.0-alpine
17)	WORKDIR app
18)	COPY . .
19)	RUN npm install
20)	EXPOSE 8000
21)	CMD ["node","app.js"]
22)	docker build . -t node-app
23)	sudo usermod -a -G docker $USER
24)	docker run -d --name node-todo-app -p 8000:8000 todo-node-app
25)	Got to jenkins job
26)	Execute shell 
27)	docker build . -t node-app-todo
28)	docker run -d --name node-app-container -p 8000:8000 node-app-todo



•	Jenkins setup: https://www.trainwithshubham.com/blog/install-jenkins-on-aws
•	https://pkg.jenkins.io/





