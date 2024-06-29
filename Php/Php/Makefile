install:
	docker-compose exec php composer install

validate:
	docker-compose exec php composer validate

up:
	docker-compose up -d

stop:
	docker-compose stop

start:
	make up && make install

build:
	docker-compose up -d --build

test:
	docker-compose exec php vendor/bin/phpunit tests/

laravel:
	docker-compose exec php composer create-project laravel/laravel ../web/

symfony:
	docker-compose exec php composer create-project symfony/skeleton ../web/

symfony-web:
	docker-compose exec php composer create-project symfony/skeleton ../web/ && docker-compose exec php composer require webapp

codeigniter:
	docker-compose exec php composer create-project codeigniter4/appstarter ../web/