# Add user to the sftp server that was created using the setup-sftp-server Ansible script 

## Purpose

```

If adding a normal user i.e. not admin the following will occur:

	- A directory for the user will be placed under /sftp/$userName where $userName is the user account name
	- The user will be added to the sftpusers group
   
If adding an admin user the following will occur:

	- Admin users do not get their own folder they get access to /sftp i.e. access to all user folders
	- Admin user gets added to sftpadmins group
	

**Remember you must manually setup a password for the user you create**

Execute as follows:

ansible-playbook -k -u <user> --inventory-file hosts playbook.yml -e "admin=<true or false> username=<username> newuser=<true or false>"

```

## Configuration

```
Add list of IP addresses to hosts file
```

## Prerequisites

```
Ansible

APT Package Manager

SSH must be installed

sftp must be setup as per the sftp-server Ansible script

```

