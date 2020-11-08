# Ansible_installation

## Step 1: Update the System
* Update the system with the latest packages and security patches using these commands.
```
sudo yum -y update
```
## Step 2: Install EPEL Repository
* EPEL or Extra Packages for Enterprise Linux repository is a free and community based repository which provide many extra open source software packages which are not available in default YUM repository.

* We need to install EPEL repository into the system as Ansible is available in default YUM repository is very old.
```
$ sudo yum install epel-release
$ sudo yum install python-argcomplete
```
* Update the repository cache by running the command.
```
sudo yum -y update
```
## Step 3: Install Ansible
* Run the following command to install the latest version of Ansible.
```
sudo yum -y install ansible
```
* You can check if Ansible is installed successfully by finding its version.
```
ansible --version
```
## Step 4:
* Do passwordless login in between controll node and Manged node
```
$ ssh-keygen
```
* Copy this generated key and paste it in manged node authorition_keys.
```
ssh-copy-id -i root@IP address of your host
```
### Note:=> Workaround: if it is not possible to copy with the help of above command then follow the following steps.
* ```cat /.ssh/id_rsa.pub``` copy it and paste it in managed node ```/.ssh/authorized_keys```
                                      ```
                                      or
                                      ```
* edit /etc/ssh/sshd_config and change ```PasswordAuthentication no``` to ```PasswordAuthentication yes```.
                                      ```
                                      or
                                      ```
* Setting 700 to .ssh and 600 to authorized_keys.
```
chmod 700 /root/.ssh
chmod 600 /root/.ssh/authorized_keys
```



