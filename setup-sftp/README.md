# Linux SFTP

## Purpose

```
Sets up sftp on server using sshd insternal-sftp server as follows:

All user directories will be placed under /sftp/$userName where $userName is the user account name
Admin will have access to /sftp
A group called sftpadmins will be created
A group called sftpusers will be created

To add users / admins use the setup-sftp-user Ansible script

Execute as follows:

ansible-playbook -k -u <user> --inventory-file hosts playbook.yml 

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

```

