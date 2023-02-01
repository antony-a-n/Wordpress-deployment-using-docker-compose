Hello folks,

According to the official documentation **docker compose** is tool which is used to define and share multiple containers.The docker compose file is written in **yaml** format.
In this example, we are installing docker-compose and setting up a wordpress website using it.

So, let's start.

Installation of docker-compose
===============================
First of all you need to install & configure docker before setting up docker-compose.

You can install &configure docker using the following steps.

```
$sudo yum install docker -y
$sudo systemctl restart docker.service 
$sudo systemctl enable docker.service
```
Once you have installed docker, you can proceed with setting up compose, follow the steps to do the same.

```
$sudo curl -SL https://github.com/docker/compose/releases/download/v2.6.0/docker-compose-linux-x86_64 -o /usr/bin/docker-compose
$sudo chmod +x /usr/bin/docker-compose
$docker-compose version
```
if it was installed successfully, you will receive the following message.

```
Docker Compose version v2.6.0
```
setting up wordpress
======================

Now we have to create our docker-compose.yml file, we can define services,volumes, network in this file.

Since we are launching a wordpress application,the containers need to be connected on  the same network.We are creating 2 services and 2 volumes. These volumes will be bind mounted to the containers.

Once you have completed writing the compose file, you can run the following command to display the expected output.

```
docker-compose config
```
If the commands in the docker-compose file are correct, it will display the expected outcome, else it will display the error.

Once you have received the outcome, you can proceed with running the containers.

```
docker-compose up -d
```
Once you have execute the above mentioned command, the containers will be active and you will be able to complete the wordpress installation process from the browser.

Thanks for reading :)



  
