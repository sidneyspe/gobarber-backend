# GoBarber Backend

Schedule, Appointments for services provider.

## Setup

You will need to install:
* nodejs
* npm
* Yarn
* [Docker](https://www.docker.com/)
* [Postbird](https://www.electronjs.org/apps/postbird)
* [Insomnia](https://insomnia.rest/download/)
* [MongoDB Compass](https://www.mongodb.com/download-center/compass)

### Docker

Please install docker and after run the following command:

`docker run -d -p 5432:5432 --name postgres -e POSTGRES_PASSWORD=postgres postgres `

This command will create a docker container with postgres installed.
The `user` and the `password` of this container is: `postgres`

`docker run --name mongo -p 27017:27017 -d -t mongo`

This command will create a docker container with mongoDB installed.

`docker run --name redis -p 6379:6379 -d -t redis:alpine`

This command will create a docker container with redis installed.

&nbsp;

After run the following command:

`docker update --restart=always postgres`

`docker update --restart=always mongo`

`docker update --restart=always redis`

This command will restart the container named postgres, mongo, redis always the docker is started.

&nbsp;

### Database
Using the Postbird or other similar app, access the postgres and create a database named:

`gobarber`

&nbsp;

### Project

Please access the `gobarber-backend` folder and run the following command: `yarn`

Run the sequelize migrations to create the tables that will need: `yarn migration`

&nbsp;


### Running the Backend Application

Please enter the command:

`yarn queue`

For running redis (queues)

&nbsp;

`yarn dev`

For running application

&nbsp;
