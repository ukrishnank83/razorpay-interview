# Razorpay-interview


For this application to work please install docker compose and docker for an ubuntu machine using the below link

https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-ubuntu-14-04


# Starting the application:

cd razorpay-interview
nohup docker-compose up & 

Logs will be stored in nohup.out in the same directory


This will run the application in the background. 
You can also use supervisorctl or setup docker-compose as a service in init.d.

# Endpoints

health_check endpoint:- /health
ping edpoint:- /ping

Logs should be giving 200 response for the above endpoint, confirming the healthy setup.

Razorpay service works on the basis of environment variables

       MYSQL_HOST: <IP or location of mysql>
       MYSQL_USER: <mysql_username>
       MYSQL_PASS: <mysql_password>
       MYSQL_PORT: <port in whicn mysql is running>
       PORT: <port for the application to run>
       GIN_MODE: release <type of release(PROD or staging)>
       
PS:- if you change the port environment variable please change port forwarding info in the docker-compose file to reflect the change.

Also the database name used by the application is razorpay








