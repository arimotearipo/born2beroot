# born2beroot
A project that will teach you about system administration

To learn about SSH service  
[Phoenix Nap article on SSH](https://phoenixnap.com/kb/how-to-enable-ssh-on-debian)

To learn about network ports and a little bit on how firewall works with network ports  
[Tech Target article on network ports](https://www.techtarget.com/searchnetworking/definition/port)

To learn about cron jobs  
[Phonix Nap article on cron jobs](https://phoenixnap.com/kb/set-up-cron-job-linux)

### __Some basic commands that will be useful for this project:__  
*Note: I am using Debian 10 for this project. There might be differences in the commands from those who are using CentOS*
1. To change the name of hostname; `$sudo hostnamectl set-hostname [NEW HOSTNAME]`
2. To check the current OS; `$cat /etc/os-release` Similarly, you can also run `$hostnamectl` to check it.
3. To check current hostname; `$hostname`
4. To list down applications; `$dpkg -l`
5. To check for the existence of a particular application; `$dpkg -l | grep [APPLICATION NAME]`
6. To switch user; `$su - [USERNAME]` If no username is entered, then you will be switched to root.
7. To add another user; `$sudo adduser [USERNAME]`
8. To delete user; `$user [USERNAME]` Use `-r` flag to delete the user's home directory as well. Use `-f` to force delete the user regardless of whether the user is still logged in
9. To rename user; `$usermod -l [NEW USERNAME] [OLD USERNAME]`
10. To list users; `$cat /etc/passd | cut -d: -f1`
11. To add a user to a group; `$sudo usermod -a -G [GROUPNAME] [USERNAME]`
12. To remove a user from a group; `$sudo gpasswd -d [USERNAME] [GROUPNAME]`
13. To create a group; `$groupadd [GROUPNAME]`
14. To delete group; `$groupdel [GROUPNAME]`
15. To list groups; `$groups`
16. To list groups of a user; `$groups [USERNAME]`
17. To list users of a group; `$cat /etc/group | grep '[GROUPNAME]`
18. To start the OpenSSH-server; `$sudo service ssh start`
19. To stop the OpenSSH-server; `$sudo service ssh stop`
20. To restart the OpenSSH-server; `$sudo service ssh restart`
21. To start UFW; `$sudo ufw enable`
22. To stop UFW; `$sudo ufw disable`
23. To check UFW status; `$sudo ufw status` This is also checks the ports currently allowed by UFW
24. To allow ports on UFW; `$sudo ufw allow [PORT NUMBER]`
25. Some other interesting UFW commands can be found [here](https://www.linux.com/training-tutorials/introduction-uncomplicated-firewall-ufw/)
26. To disallow ports of UFW; `$sudo ufw delete allow [PORT NUMBER]`
27. To edit cronjobs; `$crontab -e`
28. To check scheduled cron job on your system; `$sudo crontab -l` If you want to check scheduled cron job for a particular user; `$sudo crontab -u [USERNAME] -l`
29. 
