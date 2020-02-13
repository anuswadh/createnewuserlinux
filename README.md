# createnewuserlinux
Create a new user and add sudo access


useradd -g adm anuswadh 

sudo usermod -a -G adm anuswadh

less /etc/group

sudo vi  /etc/sudoers
#add the users with 

## Read drop-in files from /etc/sudoers.d (the # here does not mean a comment)
#includedir /etc/sudoers.d
centos  ALL=(ALL)       NOPASSWD: ALL
anuswadh  ALL=(ALL)       NOPASSWD: ALL

cd /home/anuswadh
mkdir .ssh
cd .ssh
vi authorized_keys
#copy paste the ssh key in this format

ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCDUzR+RtGaAKrZ22v2YBWbDZ7B0GLUJaM9snZJdxwMSZJkfBZ9k8fTWTRshQrV92LAc+SoBUZT+p9BQ+nE4f6XJBwyFopkEvEhuqGeb5bU06CFt5hB9jkD72zrjVt4avRF2irBKdGaADU47CoX3G51x5ccPDcsY1SAEPjvtvY2x4hirel4ZW2lSpbu7JaqFesb/0Y3pWqJ6V82oXiPs2CBXYu5TaNnrIsycnIP77M4n5qhWZzBC+et6kzpc2aN7W10g1rupHThOM5ldkfbPjPdVx3jg4RSr4ji8aTu1n/ZbpbLDS48JUYIjfgF7ouOAGOrFsC57h6rOB2gQ5xkkvgR accesForAnuswadh


