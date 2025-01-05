up:
	docker-compose up -d

stop:
	docker-compose stop

build:
	docker-compose up -d --build

restart:
	make stop && make up

run:
	docker-compose exec -T app bash -c "nohup lein run > server.log 2>&1 & jobs"
