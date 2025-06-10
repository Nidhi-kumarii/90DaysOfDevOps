Linux 

Linux is the backbone of many DevOps workflows and infrastructure, making it essential to master its core concepts and commands. In Week 2 of my journey, I focused on foundational Linux administration topics including user and group management, file permissions, volume management, networking, and powerful text-processing tools like awk, sed, and grep. Here’s a detailed look at what I learned and practiced.

Task 1

1. User & Group Management
Linux uses users and groups to control system access and resource permissions.

Users represent individual accounts on the system.

Groups are collections of users sharing common permissions.

Key system files:

`/etc/passwd` — stores user account information.

`/etc/group` — defines groups and their members.

Commands & Tasks:
```bash
#Create a user:

  sudo useradd devops_user 

##create a group 

  sudo groupadd devops_team

#add user to group :

 sudo usermod -aG devops_team devops_user 

#set user password:

 sudo passwd devops_user

#Grant sudo access by adding user to sudoers (or to sudo group):

  sudo usermod -aG sudo devops_user

#Restrict SSH login for certain user by editing /etc/ssh/sshd_config : add lines like :

  AllowUsers devops_user

#Reload SSH service after changes:

   sudo systemctl reload sshd





