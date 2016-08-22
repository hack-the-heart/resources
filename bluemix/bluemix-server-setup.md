# Setting up your Server on BlueMix

- Click on Catalog
- Under `Boilerplates`, select `Node.js Cloudant DB Web Starter`
- Enter in your app name and click CREATE

- You should be directed to the `Start Coding` screen. If not, select `Start Coding` on the left hand side.

Note: These instructions go over pushing your server code over command line. However feel free to follow the instructions for setting up Bluemix and server code on Git.

- Click on CF (Command Line Interface)
- Follow the instructions to install `CF Command Line Interface` and `Bluemix Command Line Interfaces`
- The instructions will tell you to download your starter code. However do not do this. Download the starter-nodejs-server code from HealthTechHack github repo.
- Edit your manifest.yml file (the name, host, and services)
- Setup your service credentials (by following the instructions below)
- Follow steps 5-8 on the setup guide

# Setting up your server locally
- Install NodeJS
- Run `node install` inside the folder that contains the server code to install dependencies
- Run `node start` also inside the folder that contains the server code. This is to start your nodejs server
- Visit localhost:3000/ to see your nodejs server

## Setting up Service Credentials
- Create a Service Credential for your NodeJS DB by goign to Dashboard > Services > [Your Cloudant DB] > Service Credentials
- Click on Add Credentials, Name your credential
- You should be shows a json format with username, password, host, port and url.
- Copy the json text and paste it into your config/local-db-info.json file

For now you will be connecting a local instance of your server to your server db. If you would like, you can spin up your own version of Cloudant locally and point it there when you are debugging.
