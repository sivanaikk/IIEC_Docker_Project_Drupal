# IIEC_Docker_Project_Drupal


On March 01, 2020 Indian Innovation and Entrepreneurship Community (IIEC) under the mentorship Mr.Vimal Daga started a great initiative of training Docker container technology to the persuing students from basic to advance . I am the part of the initiative and I learned a lot of things bout Docker and Containerization. Now, I am in a stage to do a project on Docker Compose.

## Drupal
Drupal is content management software. It's used to make many of the websites and applications you use every day. Drupal has great standard features, like easy content authoring, reliable performance, and excellent security. But what sets it apart is its flexibility; modularity is one of its core principles. Its tools help you build the versatile, structured content that dynamic web experiences need.

It's also a great choice for creating integrated digital frameworks. You can extend it with any one, or many, of thousands of add-ons. Modules expand Drupal's functionality. Themes let you customize your content's presentation. Distributions are packaged Drupal bundles you can use as starter-kits. Mix and match these components to enhance Drupal's core abilities. Or, integrate Drupal with external services and other applications in your infrastructure. No other content management software is this powerful and scalable.

The Drupal project is open source software. Anyone can download, use, work on, and share it with others. It's built on principles like collaboration, globalism, and innovation. It's distributed under the terms of the GNU General Public License (GPL). There are no licensing fees, ever. Drupal will always be free.

## 1. Pre-Configuration :
REDHAT ENTERPRISES LINUX 8 and installed with Docker and Docker Compose .
* we need to download mysql to check database
```
dnf install mysql
```

## 2. Install Docker 
* Install docker 
``` 
dnf install docker-ce
```
* start docker 
```
systemctl start docker 
```
* To check the status of docker 
```
systemctl status docker 
```
**Disable firewall if Docker is dead**

## 3.Required Images 
I am using the MySQL as database to the ghost. mysql:5.7 and ghost:1-alphine images from docker hub

* To pull mysql
```
docker pull mysql:5.7
```
* To pull ghost
```
docker pull drupal:latest
```

## 4. Install Docker Compose 
* We need to download docker compose software . Follow the instructions in the link to install docker compose
https://docs.docker.com/compose/install/
* The docker compose file must be **docker-compose.yml** . we have to check every time we create the docker compose file.

## 5. Docker-Compose
* Write in **docker-compose.yml** file

![docker-compose.yml](/drupal_vim.png?raw=true)

from above screen shot :

**version**  is the version of the docker compose we are using.

**services** specify about the running services in docker 

**volume** are the storage units for services

**image** specifies about the image we are using 

**evironments** are the variables to specify before starting of the container

**restart** is to restart the service if it any containers start

**port** is to specify particular service 

**depends_on** is to specify it depends on database to store data



## 6.Docker-Compose Up

* To start docker compose
```
docker-compose up -d 
```

* To stop the docker compose
```
docker-compose stop
```

* To start the docker compose
```
docker-compose start
```
![docker-compose.yml](/drupal_upd.png?raw=true)

## 7.Launch the Web App 
Open the browser and search with IP Address and Port mentioned .
![docker-compose.yml](/drupal_launch.png?raw=true)

### we can also launch the webapp manually without using the docker compose 

### All credits goes to Vimal Daga sir. Thank you Vimal Daga sir for training the Docker in such a level that I can do projects.
