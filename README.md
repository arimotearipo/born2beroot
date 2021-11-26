# born2beroot
A project that will teach you about system administration

To learn a bit about Virtual Machine (VM) and why use them  
[DNS Stuff article on VM](https://www.dnsstuff.com/what-is-vm-virtual-machine)

To learn about what is apt and what is Aptitute  
[Tecmint article on apt and Aptitute](https://www.tecmint.com/difference-between-apt-and-aptitude/)

To learn about a few differences between CentOS and Debian  
[OpenLogic article on CentOS vs Debian](https://www.openlogic.com/blog/centos-vs-debian)

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
4. To list down applications/programmes; `$dpkg -l` Similarly, you can also use `$apt list --installed`
6. To check for the existence of a particular application; `$dpkg -l | grep '[APPLICATION NAME]'` Similarly, you can use `$apt list --installed | grep '[APPLICATION NAME]'` 
7. To switch user; `$su - [USERNAME]` If no username is entered, then you will be switched to root.
8. To add another user; `$sudo adduser [USERNAME]`
9. To delete user; `$user [USERNAME]` Use `-r` flag to delete the user's home directory as well. Use `-f` to force delete the user regardless of whether the user is still logged in
10. To rename user; `$usermod -l [NEW USERNAME] [OLD USERNAME]`
11. To list users; `$cat /etc/passd | cut -d: -f1`
12. To add a user to a group; `$sudo usermod -a -G [GROUPNAME] [USERNAME]`
13. To remove a user from a group; `$sudo gpasswd -d [USERNAME] [GROUPNAME]`
14. To create a group; `$groupadd [GROUPNAME]`
15. To delete group; `$groupdel [GROUPNAME]`
16. To list groups; `$groups`
17. To list groups of a user; `$groups [USERNAME]`
18. To list users of a group; `$cat /etc/group | grep '[GROUPNAME]`
19. To start the OpenSSH-server; `$sudo service ssh start`
20. To stop the OpenSSH-server; `$sudo service ssh stop`
21. To restart the OpenSSH-server; `$sudo service ssh restart`
22. To start UFW; `$sudo ufw enable`
23. To stop UFW; `$sudo ufw disable`
24. To check UFW status; `$sudo ufw status` This also checks the ports currently allowed by UFW
25. To allow ports on UFW; `$sudo ufw allow [PORT NUMBER]`
26. To disallow ports of UFW; `$sudo ufw delete allow [PORT NUMBER]`
27. Some other interesting UFW commands can be found [here](https://www.linux.com/training-tutorials/introduction-uncomplicated-firewall-ufw/)
28. To edit cronjobs; `$crontab -e`
29. To check scheduled cron job on your system; `$sudo crontab -l` If you want to check scheduled cron job for a particular user; `$sudo crontab -u [USERNAME] -l`
30. To list partitions; `$lsblk` 
