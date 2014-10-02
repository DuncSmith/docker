all: build

build:
	docker build -t duncsmith/minecraft-server .

run:
	docker run -d -p 25565:25565 -v /data/mc:/data/world --name="minecraft-server" duncsmith/minecraft-server

stop:
	docker stop minecraft-server

clean: stop
	docker rm minecraft-server

purge:
	docker rmi duncsmith/minecraft-server:latest