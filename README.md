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
5. Change `BASE_URL` environment variable inside `Onlinecalculatorfrontend/config/prod.env.js` to production server's ip address or domain name 
   ``` javascript
    'use strict'
    module.exports = {
    NODE_ENV: '"production"', 
    BASE_URL: '"http://<ip_address/domain>:8000/"'
    }
6. Add server's domain name or public IP address to `ALLOWED_HOSTS` variable in `Onlinecalculator/onlinecalculator/settings.py`
   ``` python
   ALLOWED_HOSTS = ['<ip address or domain name here>']
   ```
7. Build the docker-images
   ``` bash
    docker-compose build
   ```
## Starting/Stopping the online calculator (must by inside this repo when executing `docker-compose` commands)
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
