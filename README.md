DOCKER COMPOSE TOOL TO CREATE INFRASTRUCTURE FOR MULTI-CONTAINER INSTALLATION

To run this YAML file and start your services using this infrastructure, you must have a server running linux OS(here I am using RHEL8), along with root user privileges and firewall setup for configured.
You must have Docker along with Dcoker-compose tool installed on your server.
setup the same configuration for nginx web server.
Start your docker service : "systemctl start docker"
To start your services :  "docker-compose up -d" this will run your conatiners in background.you will see it will start pulling the required images from docker repository,if not downloaded else it will start all the containers.
Use this command "docker-compose ps" to see the status of your containers.
You can now check that your certificates have been mounted to the webserver container "docker-compose exec webserver ls -la /etc/letsencrypt/live".
Now that you know your request will be successful, you can edit the certbot service definition to remove the --staging flag.Open yml file and edit.Find the section of the file with the certbot service definition, and replace the --staging flag in the command option with the --force-renewal flag, which will tell Certbot that you want to request a new certificate with the same domains as an existing certificate. You can now run docker-compose up to recreate the certbot container. We will also include the --no-deps option to tell Compose that it can skip starting the webserver service, since it is already running : "docker-compose up --force-recreate --no-deps certbot. You will see output indicating that your certificate request was successful. With your certificates in place, you can move on to modifying your Nginx configuration to include SSL. With your containers running, you can now complete your WordPress installation through the web interface.  


                                                                          
