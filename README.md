# onlinecalculator-docker-setup

## Setup
1. Install Docker on production server using official channel: https://docs.docker.com/install/
2. Clone this repository and go inside the repository
   ``` bash
    git clone https://github.com/musqueteers/onlinecalculator-docker-setup
    cd onlinecalculator-docker-setup
   ```
3. Clone frontend repository inside repository
   ``` bash
    git clone https://github.com/musqueteers/Onlinecalculatorfrontend
   ```
4. Clone backend repository inside repository
    ``` bash
    git clone https://github.com/musqueteers/Onlinecalculator
   ```
5. Change `VUE_APP_BACKEND_ADDR` environment variable inside `docker-compose.yml` to production server's ip address or domain name 
   ``` yaml
    VUE_APP_BACKEND_ADDR: "<ip_address/domain">
   ```
6. Build the docker-images
   ``` bash
    docker-compose build
   ```
## Starting/Stopping the online calculator
1. Starting the application
    ``` bash
    docker-compose up &
    ```
2. Stopping the application
    ``` bash
    docker-compose down
    ```

## Other useful commands:
1. Show logs (should be inside this repo):
    ``` bash
    docker-compose logs
    ```
1. Show running docker-compose services (should be inside this repo):
       ``` bash
    docker-compose ps
    ```