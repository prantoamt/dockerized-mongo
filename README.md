### Table of Contents  
---------------------

- [Before you start](#before-you-start)
- [Quick Start](#quick-start)
    + [Install pdm as python package manager](#install-pdm-as-python-package-manager)
    + [Clone repo](#clone-repo)
    + [Goto the base directory](#goto-the-base-directory)
    + [Install the dependencies](#install-the-dependencies)
    + [Run the project](#run-the-project)
    + [See project in action](#see-project-in-action)
- [Api](#api)


# Before you start
----------------------------
Hello! Welcome to the my dockerized mongodb repository. 
This repository contains a simple setup with docker-compose to run mongo image on your local machine.
This `readme.md` file will guide you to run the container. 
I presume you have docker installed in your local machine.
The section [Quick Start](#quick-start) has all the required steps to run the container. Before that, please read the following notes:

- Docker image mongo:6.0.3 has been used as mongodb image
- Port mapping `27017:27017` has been used to map the internal and external mapping. **So, 27017 should be a free port to run the container**


# Quick Start
-----------------
Please pursue the following steps.

#### Clone repo
--------------------
Clone this git repository to your local machine. Open your terminal and run the command

```
git clone git@github.com:prantoamt/dockerized-mongo.git
```
If SSH does not work, please try with HTTPS:
```
git clone https://github.com/prantoamt/dockerized-mongo.git
```

#### Goto the base directory
------------------------------------
After cloning the repo, goto the base directory by executing the following command: 
```
cd dockerized-mongo
```

#### Create an .env file
-----------------------------------------------------------------
Create a `.env` file inside the directory which will contain your database's credentials.
```
touch .env
```

### Write your credentials in the .env file
-------------------
Open the `.env` file with your prefered code editor and set the values for the following variables.
Replace *your_database_name, your_root_user, and your_root_user_password* with your credentials.
```
MONGO_INITDB_DATABASE = your_database_name
MONGO_INITDB_ROOT_USERNAME = your_root_user
MONGO_INITDB_ROOT_PASSWORD= your_root_user_password
```

### Run the container
-------------------------
Run the container with `docker-compose`

```
docker-compose up -d --build
```

## Access your db with mongodb tools
--------------------------------------
Contratulations! You can now access your database with any tools by using
the credentials you have provided in the `.env` file.