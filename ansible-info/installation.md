# Install Ansible on CentOS 8:
* Let's look at the installation steps for CentOS 8. Let's install python on CentOS 8.
```
$sudo dnf install python3
```
* Once, python is installed, let's install EPEL repo by executing the below command.
```
$sudo dnf install epel-release -y
```
* Update the system package index by executing the below update command.
```
$sudo dnf update -y
```
* We are now ready to install Ansible. Execute the below command to install Ansible.
```
$sudo dnf install ansible -y
```
* Verify if Ansible is installed properly and it's version. 
```
$ansible -v
```
---
# Install Ansible on Ubuntu:
* Python is a default package nowadays in most of the Linux distributions.  
If you don't have python installed, execute the below command to install the python package. 
```
$sudo apt-get install python3
```
* To install Ansible in Ubuntu, let's first install the repository by executing the below command. 
```
$sudo apt-add-repository ppa:ansible/ansible
```
* Update the system package index by executing the below update command.
```
$sudo apt-get update -y
```
* Now, install Ansible.
```
$sudo apt-get install -y ansible
```
* Verify if Ansible is installed properly and it's version. 
```
$ansible -v
```
(Remember to check if the python application is installed and it meets the version required.  
 if you want to update your python version , follow [this](https://github.com/amirsalehag/programming/blob/main/python-info/installation.md) instruction.)
