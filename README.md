DOCKER COMPOSE TOOL TO CREATE INFRASTRUCTURE FOR MULTI-CONTAINER INSTALLATION

 I am going to show how Docker and compose tool can help in management of infrastructure. I am going to create a WordPress as my infrastructure.WordPress is free and open-source Content management System(CMS) built on MySql database with PHP processing. It is a popular choice when creating different types of websites,from blogs to product pages to ecommerce sites. Running WordPress typically involves installing a LAMP,which includes Linux,Apache,MySql and PHP or LEMP,which includes Linux,Nginx,MySql and PHP stacks.This installation can be time consuming. Instead of installing individual components by hand,i will be using their images and run these images in containers and isolate each processes.And then,with the help of docker compose tool,we can coordinate multiple containers to communicate with each other. I am going to build a multi-container WordPress installation. I will be having a MySql database,an nginx web server and wordpress itself. I will also secure my installation by certbot by obtaining TLS/SSL certificates with Let's Encrypt for domain we want to associate with our site. We need to have setup DNS A record for our server to use our registered domain and before running any containers,we need to define the configuration for our Nginx web server. I have attached the configuration file for nginx web server.       

                                                                          
