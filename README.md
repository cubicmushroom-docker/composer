Composer Docker Container
=========================

Docker image to perform composer tasks.


Usage
-----

### Using docker

Composer install…

    $ docker run --user $(shell id -u):$(shell id -g) -v ~/.composer:/.composer -v .:/var/www/html cubicmushroom/composer install
    # or, as default command is install
    $ docker run --user $(shell id -u):$(shell id -g) -v ~/.composer:/.composer -v .:/var/www/html cubicmushroom/composer

Composer update…

    $ docker run --user $(shell id -u):$(shell id -g) -v ~/.composer:/.composer -v .:/var/www/html cubicmushroom/composer update

Composer require…

    $ docker run --user $(shell id -u):$(shell id -g) -v ~/.composer:/.composer -v .:/var/www/html cubicmushroom/composer require symfony/symfony


### Using docker-compose

#### `docker-composer.yml` file

    # docker-composer.yml
    version: '2'
    services:
      composer:
        image:          cubicmushroom/docker-composer
        container_name: limtool_api_composer
        volumes:
          - ~/.composer:/.composer
          - .:/src

#### Commands…

Composer install…

    $ docker-compose run --user $(shell id -u):$(shell id -g) composer install
    # or, as default command is install 
    $ docker-compose run --user $(shell id -u):$(shell id -g) composer 

Composer update…

    $ docker-compose run --user $(shell id -u):$(shell id -g) composer update

Composer require…

    $ docker-compose run --user $(shell id -u):$(shell id -g) composer require symfony/symfony