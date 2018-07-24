# Data-Science-Toolkit-Assignment

1) Bash: commands-

mkdir –p .ssh

ssh-keygen

#do not enter passphrase#
 
2) Amazon Web Services:
Login -> services -> EC2 -> Security Groups -> create security group

Inbound -> Type ->  SSH                      [22]        anywhere
                                             HTTP                                 [80]         “”
                                             HTTPS                   [443]  “”
                                             Postgres SQL                 [5432]  “”
                                        Custom TCP   [27016] “”
 
Services -> EC2 Dashboard-> launch instance -> Choose AMI (Ubuntu Server 16.04) -> t2.micro -> add storage (20 Gib) -> configure security group (check the Key Pair that was created) -> launch instance
 
3) Bash:

ssh Ubuntu@<IPaddress>

curl –sSL https://get.docker.com | sh

sudo username –aG docker Ubuntu

exit

<up arrow>

tmux

docker –v

docker pull jupyter/datascience-notebook

docker images

docker run \

> -d \

> -p 443:8888 \

> -v /home/ubuntu:/home/jovyan \

> jupyter/datascience-notebook

ps

docker ps

docker stop <given adjective_name>

docker ps –a

vi .profile

#move cursor down#

:wq #closes it#

echo 'alias j= "docker run -d -p 443:8888 -v/home/ubuntu:/home/jovyan jupyter/datascience-notebook"' >> .profile

source.profile

j

docker rm –f 10

source .profile

j

docker ps #see it running#

j               #gives loud error#

docker ps #get container id#

docker exec <container id> jupyter notebook list

#go to AWS IP address url#

#copy and paste the token#

create a notebook

