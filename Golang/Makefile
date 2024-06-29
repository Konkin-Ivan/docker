up:
	docker-compose up -d

down:
	docker-compose stop

start:
	make up && make install

build:
	docker-compose up -d --build

run:
	docker-compose exec golang go run main.go

test:
	docker-compose exec golang go test ./...