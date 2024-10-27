# Docker-Setup-Process

### Step 1: Install Docker
- Install Docker from the official website: https://docs.docker.com/get-docker/
- Verify the installation by running the following command in the terminal:
```bash
docker --version
```
### Step 2: Install Docker Compose
- Install Docker Compose by running the following command in the terminal:
```bash
sudo apt install docker-compose
```

### Step 3: Copy the file and folder structure

- Copy ```docker-compose.yml``` and ```.docker``` folder to the root directory of your project.
- The ```.docker``` folder contains the following files:
  - ```Dockerfile```: Contains the instructions to build the Docker image.
  - ```mysql```: Contains the configuration for the MySQL database.
  - ```nginx```: Contains the configuration for the Nginx server.
  - ```php```: Contains the configuration for the PHP server.
  - ```start.sh```: Contains the command to start the application.
- The ```docker-compose.yml``` file contains the configuration for the Docker Compose service.
- The ```nginx->conf.d->app.conf``` to change ```fastcgi_pass "your-service-name":9000;```.
  - .env file contains the environment variables for the application.
  ```bash
    DB_CONNECTION=mysql
    DB_HOST=serviceName_db
    DB_PORT=3306
    DB_DATABASE=your_database_name
    DB_USERNAME=your_database_username
    DB_PASSWORD=your_database_password
```
