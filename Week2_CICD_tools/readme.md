1. sudo apt update<br />
sudo apt install openjdk-8-jdk <br />
sudo apt-get update<br />
sudo apt-get install jenkins<br />
sudo systemctl enable jenkins.service<br />
sudo vi /etc/default/jenkins ( changed HTTP_PORT=8080 to HTTP_PORT=8081)<br />
sudo systemctl restart jenkins.service 
sudo cat /var/lib/jenkins/secrets/initialAdminPassword (pasted password to Jenkins web)<br />
<img width="594" alt="Screenshot 2021-10-16 at 15 09 35" src="https://user-images.githubusercontent.com/86781900/137587050-89e2ba6b-faba-4a43-bbb0-8bd0685740ec.png">
Manage Jenkins -> Manage Plugins -> install GitHub and Role-based authorization strategy <br />
 Manage Jenkins -> Manage Users -> created new user “jenkins-mariiaheirasymenko” <br />

2. sudo apt update <br />
sudo apt install openjdk-8-jre-headless <br />
sudo useradd --shell /bin/bash <br />
su jenkins <br />
sudo mkdir /home/jenkins <br />
ssh-keygen -t rsa <br />
cat /home/jenkins/.ssh/id_rsa.pub > /home/jenkins/.ssh/authorized_keys <br />
Manage Jenkins -> Manage Credentials -> pasted private key <br />
Manage Jenkins -> Manage Nodes and Clouds -> Created new node <br />
<img width="1044" alt="Screenshot 2021-10-17 at 12 55 34" src="https://user-images.githubusercontent.com/86781900/137622083-233b28c9-3942-4d11-8cd8-cb3b69715e96.png">


3. Install plugin NodeJs<br />
Configure Nodejs<br />

<img width="845" alt="Screenshot 2021-10-17 at 10 23 16" src="https://user-images.githubusercontent.com/86781900/137640582-6f21d892-02db-4fd7-9bc7-56a626bd6445.png">

4. <img width="730" alt="Screenshot 2021-10-17 at 21 39 49" src="https://user-images.githubusercontent.com/86781900/137640549-3970ec0b-da71-4049-bbee-7af860ee85c1.png">
<img width="963" alt="Screenshot 2021-10-17 at 18 22 48" src="https://user-images.githubusercontent.com/86781900/137640556-92d847b5-3dd4-459f-ad97-6aec9ac8d38f.png">
<img width="1049" alt="Screenshot 2021-10-17 at 18 26 31" src="https://user-images.githubusercontent.com/86781900/137640563-1df909e0-82a4-4279-affb-a4fd213bcbd2.png">

5. Install Multibranch Scan Webhook Trigger <br />
Scan by webhook <br />
Github: Setting/webhooks/created webhook <br />
<img width="971" alt="Screenshot 2021-10-17 at 18 10 48" src="https://user-images.githubusercontent.com/86781900/137633397-2eef94f2-171b-4c0f-b8d6-084c711dc9cc.png">

