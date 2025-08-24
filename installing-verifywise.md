---
description: 'Estimated setup time: approximately 30 minutes'
---

# 💾 Installing VerifyWise

Please see the installation and running instructions [here](https://github.com/bluewave-labs/verifywise).

There are two ways of installing VerifyWise. The first method is for developers (for testing/developing), and the second one is to deploy VerifyWise on a Linux server (for production systems).

## Option 1: Installing VerifyWise via npm (for developers)

### Prerequisites

1. Install `npm`: Ensure you have npm installed on your system.
2. Install Docker: Make sure Docker is installed.
3. Download Docker PostgreSQL Image: Get PostgreSQL Docker image, version 16.8.

#### 1. Clone the repository

Clone the repository (main branch) to your local machine.

#### 2. Install dependencies

Navigate to the Clients directory and install the dependencies:

```
cd Clients
npm i
```



\


Navigate back to the root directory and then to the Servers directory to install the dependencies:

cd ..

cd Servers

npm install

\


Create a .env file in the root directory:

touch .env

Copy the contents of .env.dev to the .env file:

cp .env.dev .env

#### 4. Run PostgreSQL with Docker

Run the PostgreSQL container with the following command:

docker run -d --name mypostgres -p 5432:5432 -e POSTGRES\_PASSWORD={env variable password} postgres\
\


Access the PostgreSQL container and create the verifywise database:

\


docker exec -it mypostgres psql -U postgres

CREATE DATABASE verifywise;

\


Navigate to the Servers directory and start the server in watch mode:

\


cd Servers

npm run watch

\


Navigate to the Clients directory and start the client in development mode:

\


cd Clients

npm run dev

\
\[Note: Make sure to replace {env variable password} with the actual password from your environment variables. ]

\
\


Setup and Run Instructions using docker

### Prerequisites

* Ensure you have the following installed:
*
  * npm
  * Docker
  * Docker Compose

Create Directory

Create a directory in your desired folder:

mkdir verifywise

cd verifywise

Download Necessary Files

Download the required files using wget:

wget https://raw.githubusercontent.com/bluewave-labs/verifywise/develop/install.sh

wget https://raw.githubusercontent.com/bluewave-labs/verifywise/develop/docker-compose.yml

wget https://raw.githubusercontent.com/bluewave-labs/verifywise/develop/.env.prod

Create Servers Directory

Create a Servers directory and download the SQL commands file:

mkdir Servers

cd Servers

wget https://raw.githubusercontent.com/bluewave-labs/verifywise/develop/Servers/SQL\_Commands.sql

cd ..

\


Make Install Script Executable

Change the permissions of the install.sh script to make it executable:

chmod +x ./install.sh

Execute the install.sh script:

./install.sh

### Troubleshooting

If the install.sh script doesn't work, try the following commands:

docker-compose --env-file .env.prod up -d backend

docker ps  # to confirm

docker-compose --env-file .env.prod up -d frontend

docker ps  # to confirm

\
\


