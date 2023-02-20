## Setup

- Clone the repository
  ```bash
  git clone https://github.com/PRINCESS-D/laravel.git
  ```

- Make sure you have the latest version of [Composer](https://getcomposer.org/download/) installed

- Make use of composer to create project in the downloaded folder
  ```bash
  cd laravel
  composer create-project
  ```

- Once you have the project setup, there's a docker-compose.yml file in the root directory. Make sure you have [Docker](https://docs.docker.com/get-docker/) installed and run the following command to start the containers
  ```bash
  docker-compose up
  ```

- The docker file for the application can be found in `vendor/laravel/sail/runtimes/8.2/Dockerfile` and that is the one that is being used to build the image for the application and is referenced in the `docker-compose.yml` file

- The docker-compose.yml file has the following services
  - `laravel.app` - This is the application service
  - `mysql` - This is the database service
  - `redis` - This is the redis service
  - `meilisearch` - This is the search service
  - `mailpit` - This is the mail service
  - `selenium` - This is the selenium service

- The `.env` file has all the necessary environment variables for the application to run. The docker-compose uses the `.env` file to set the ports for the services and the environment variables for the application service

- Once the containers are up and running, you can access the application at [http://localhost:8080](http://localhost:8080)