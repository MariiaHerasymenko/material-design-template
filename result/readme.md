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

