# Bionic Yoshi Client

## Prerequisites
**yarn 1.9.4** or **node 8.11.1** (or higher) is required

## Installation
This application can be installed via **yarn** by running `yarn`.

### Configuration
You can find a configuration file at `/src/conf.js` if you need. 

You have to configure URL:PORT of API and WebSocket Server in PROD MODE


### Build
Once installed you're able to build the client. Make sure that your **server** is running properly.

#### Development mode
To launch the client in dev mode, run `yarn start`. 

You can access your project at : [http://localhost:8080](http://localhost:8080)

#### Production mode
To build the client in prod mode, run `yarn build`.

You can use Nginx config to serve dist folder.

````
server {
   listen 80 default_server;
   root /var/www/jsfullstackclient/dist;
   server_name 35.233.61.218;
   index index.html index.htm;
   location / {
    try_files $uri /index.html =404;
   }
}
````

#### Accessing the application
Go to [http://35.233.61.218](http://35.233.61.218) to our hosted version (may not be up to date).