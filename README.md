# diabetes-detection
this repo is for diabetes-detection using machine learning  and create docker images  

for building a docker images we need to install docker 

here iam using flasgger for ui 

for windows:
==========
https://download.docker.com/win/stable/Docker%20Desktop%20Installer.exe

after installing build a docker images

clone this repo by using git.

step1 :

go to /app folder

and then excute commands:
=======================

docker build -t diabetis:v1 .     #note v1 '.' is necessary

docker -d -p 5000:5000 --name diabetis diabetis:v1

see if you want to see output remove -d from dcoker build 


docker commands:
=================
docker images   # to see the images

docker ps       # to see the running contaiers

docker ps -a    # to see all containers

docker rmi <imagename or id>   # to remove the image
  
docker rm -f $(docker ps -a -q)   # to remove alll containers

docker rmi -f $(docker images -q) # to remove all images

docker exec -it <containerid or contiainer name> /bin/bash      # to login to container
 

note:
===
if u are using loadbalancer in cloud then change nodeport to loadbalancer in diabetis.yaml



