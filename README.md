# alyce-server
The Node Server managing Alyce's Clients and Frontend

## COMMAND TO INSTALL THE REQUIRED TOOLS

01. sudo apt-get update
02. curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
03. sudo apt-get install -y nodejs
04. sudo npm install npm --global
05. sudo npm install pm2 -g
07. sudo apt install nginx

## COMMAND TO FETCH THE LATEST SERVER CODE

01. git clone https://github.com/alyce-garner-peterson/alyce-server.git
02. git pull

## COMMAND TO SET THE NGINX CONFIGURATION( Modify if required to change the ports, SSL Certificate, etc... )

01. sudo unlink /etc/nginx/sites-enabled/default
02. sudo cp ./NGINX_Configuration_Files/configurationHttp /etc/nginx/sites-available/configurationHttp
03. sudo ln -s /etc/nginx/sites-available/configurationHttp /etc/nginx/sites-enabled/configurationHttp

## COMMAND TO START THE SERVERS AS BACKGROUND PROCESSES( Modify config.js for changing server port)

01. sudo pm2 start "npm start" --name AlyceServer

## COMMAND TO RESTART THE NGINX SERVICE WITH NEW CONFIGURATIONS

01. sudo service nginx restart