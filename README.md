Composer Docker Container
=========================

Docker image to perform composer tasks.


Usage
-----

Composer install…

    $ docker run --user $(shell id -u):$(shell id -g) -v .:/var/www/html cubicmushroom/composer install
    # or 
    $ docker run --user $(shell id -u):$(shell id -g) -v .:/var/www/html cubicmushroom/composer

Composer update…

    $ docker run --user $(shell id -u):$(shell id -g) -v .:/var/www/html cubicmushroom/composer update

Composer require…

    $ docker run --user $(shell id -u):$(shell id -g) -v .:/var/www/html cubicmushroom/composer require symfony/symfony