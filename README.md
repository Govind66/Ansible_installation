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
sudo yum -y install epel-repo
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
