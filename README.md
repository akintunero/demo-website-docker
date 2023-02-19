## demo app - NGINX-Docker



This demo app is a sample Static Webiste built with 

-   HTML
-   CSS
-   NGINX
-   Docker

This demo website uses docker volume to share the website files thats built locally with docker.

### To install NGINX

Step 1:

From the directory your webiste files are hosted locally, pull and run NGINX with the docker volume flag -v:

        docker run --name demo-website -d -v $(pwd):/usr/share/nginx/html:ro -d -p 8080:80 nginx:alpine



#### Write a Dockerfile to build a docker container for the website:

Step 2:

        FROM nginx:alpine
        ADD .  /usr/share/nginx/html
        EXPOSE 80
    

#### Build the docker image for the webiste

Step 3:

        docker build -t demo-website:latest .

#### Run the container locally

Step 4:

        docker run -d -p 8080:80 demo-website:latest .


#### Launch the Docker Image on the UI

Step 5:
 
 Launch the UI from a web browser using:
 
        localhost:8080


![image](https://user-images.githubusercontent.com/13016369/219940663-68f7de40-7b0d-4834-beae-81d89f6b0a7e.png)





        

Website Credit:

Template Name: HeroBiz
Template URL: https://bootstrapmade.com/herobiz-bootstrap-business-template/
Author: BootstrapMade.com
License: https://bootstrapmade.com/license/
