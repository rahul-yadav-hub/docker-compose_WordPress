DOCKER COMPOSE TOOL TO CREATE INFRASTRUCTURE FOR MULTI-CONTAINER INSTALLATION

>>>To run this YAML file and start your services using this infrastructure, you must have a server running linux OS(here I am using RHEL8), along with root user privileges and firewall setup for configured.
>>>You must have Docker along with Dcoker-compose tool installed on your server.
>>>setup the same configuration for nginx web server.
>>>Start your docker service : "systemctl start docker"
>>>To start your services :  "docker-compose up -d" this will run your conatiners in background.you will see it will start pulling the required images from docker repository,if not downloaded else it will start all the containers.
>>>Use this command "docker-compose ps" to see the status of your containers.
>>>You can now check that your certificates have been mounted to the webserver container "docker-compose exec webserver ls -la /etc/letsencrypt/live".
>>>Now that you know your request will be successful, you can edit the certbot service definition to remove the --staging flag.Open yml file and edit.


                                                                          
