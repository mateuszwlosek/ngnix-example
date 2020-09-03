# Ngnix - Example

Simple example of [Ngnix](https://www.nginx.com/) proxy with [Spring Boot](https://projects.spring.io/spring-boot/).  

Used [Docker](https://www.docker.com/) to containerize environment.  

## Ngnix
* Ngnix uses self signed certificate as an example. Browser will warn about not secure connection. This is just an example, for real production case, real SSL certificates have to be bought  
Generating example certificate:  
`openssl req -newkey rsa:2048 -new -nodes -x509 -days 3650 -keyout key.pem -out cert.pem`  
* This example only allows to forward request and use https but it is open for modifications
 
## How to run the environment?

### Before you start
* Make sure you have `Docker` and `docker-compose` installed.

[Docker CE INSTALLATION](https://docs.docker.com/install/linux/docker-ce/ubuntu/)  
[Docker Compose INSTALLATION](https://docs.docker.com/compose/install/#prerequisites)

### Start the environment
1. Build services:
    `docker-compose build`
2. Run services:
    `docker-compose up`

### Important endpoints:
* https://localhost/test - Test endpoint from example-service
