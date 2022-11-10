# Example Laravel API Application

## Get started
1) Copy over the ```.env.example``` file to ```.env```
``` bash
    cp .env.example .env
```
2) Run composer install using the following [Docker](https://www.docker.com/) command:
``` bash
docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v $(pwd):/var/www/html \
    -w /var/www/html \
    laravelsail/php81-composer:latest \
    composer install --ignore-platform-reqs
```
3) Run the following command to launch the sail containers
``` bash
./vendor/bin/sail up
```
You can also append the ```-d``` flag to the command above to run in detached mode.
``` bash
./vendor/bin/sail up -d
```
4) visit [localhost](http://localhost/) to view your application.

## Helpful Things
- Useful shell alias for sail
``` bash
alias sail='[ -f sail ] && sh sail || sh vendor/bin/sail'
```