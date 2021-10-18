2. sudo apt update<br />
   sudo apt install nginx<br />
3. fork GitHub repo<br />
   ssh-keygen<br />
   (pasted id_rsa.pub to Github SSH key)<br />
   git config --global user.name MariiaHerasymenko<br />
   git config --global user.email msgerasymenko@gmail.com<br />
   git clone git@github.com:MariiaHerasymenko/material-design-template.git<br />
   cd /etc/nginx/sites-enabled<br />
   vi default (changed route to index.html)<br />
   sudo systemctl restart nginx<br />
4. crontab -e  (***** cd /home/msgerasymenko/material-design-template && git pull origin master)<br />

<img width="899" alt="Screenshot 2021-10-09 at 16 35 00" src="https://user-images.githubusercontent.com/86781900/136700925-52c23b94-ea4d-4fa0-a117-f333e9bb0bf8.png">

5. vi index.html (did some changes) <br />
   git add index.html <br />

   git commit -m "Changed index.html"<br />
   git push origin master<br />
6. In /home/msgerasymenko/example/.git/hooks created pre-commit file (add executable permission):

<img width="495" alt="Screenshot 2021-10-10 at 16 55 01" src="https://user-images.githubusercontent.com/86781900/136700995-819f1049-2b91-4355-bdc4-6fff221a4299.png">

7. From server side:<br />
sudo apt-get install nodejs npm<br />
sudo ln -s /usr/bin/nodejs /usr/local/bin/node<br />
npm init (created package.json file)<br />
sudo npm install ws<br />
touch server.js <br />
Pasted these contents:<br />
<img width="483" alt="Screenshot 2021-10-14 at 16 22 54" src="https://user-images.githubusercontent.com/86781900/137326257-aaec8279-9af7-41e9-a34f-8e4c30d9c201.png">
sudo vi /etc/nginx/sites-available/websocket<br />
node server.js<br />

From client side:<br />
curl -i -N -H "Connection: Upgrade" -H "Upgrade: websocket" -H "Host: echo.websocket.org" -H "Origin: http://www.websocket.org" http://34.125.201.185
<img width="863" alt="Screenshot 2021-10-14 at 20 30 18" src="https://user-images.githubusercontent.com/86781900/137367596-5b014562-8772-4e59-a23e-fc6d028bda02.png">

From server side:<br />
sudo vi /etc/nginx/sites-enabled/default<br />

<img width="768" alt="Screenshot 2021-10-14 at 23 02 16" src="https://user-images.githubusercontent.com/86781900/137387385-502bc25e-7a43-49de-af15-71861ddfc01d.png">

sudo nginx -s reload<br />
curl -i http://34.125.201.185/img/avatar1.png<br />

<img width="617" alt="Screenshot 2021-10-14 at 23 03 59" src="https://user-images.githubusercontent.com/86781900/137387580-5d842c76-ec0b-432f-b00d-d4a481aba77d.png">
8. git checkout -b feature<br />
   (Add some changes in existing file)<br />
   git add .<br />
   git commit -m “Feature changes”<br />
   git checkout master<br />
   (add some changes in existing file)<br />
   git add .<br />
   git commit -m “Master changes”<br />
   git merge feature<br />
   (resolved conflict in a file)<br />
   git add .<br />
   git commit -m “Resolved conflict”<br />
   git log —graph<br />

<img width="717" alt="Screenshot 2021-10-10 at 17 37 03" src="https://user-images.githubusercontent.com/86781900/136700863-10ea123e-ef4c-4fe9-b895-3a104f30024c.png">

   git rebase feature<br />
   (Resolved conflict in a file)<br />
   git add .<br />
   git rebase —continue<br />
   git log —graph<br />

<img width="687" alt="Screenshot 2021-10-10 at 17 45 42" src="https://user-images.githubusercontent.com/86781900/136700818-19625643-6e66-4649-b446-9e22da7db3dd.png">
 
   git rebase -i<br />
<img width="665" alt="Screenshot 2021-10-10 at 17 57 20" src="https://user-images.githubusercontent.com/86781900/136701269-828f45dc-8432-424b-8a05-5ef40ef7c6ee.png">

