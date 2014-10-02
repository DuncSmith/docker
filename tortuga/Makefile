all: build

build:
	docker build -t duncsmith/tortuga .

run:
	docker run -d -v /data/tortuga:/tortuga -p 8081:8081 -p 8080:8080 -p 9090:9090 --name="tortuga" duncsmith/tortuga

stop:
	docker stop tortuga

clean: stop
	docker rm tortuga

purge:
	docker rmi duncsmith/tortuga:latest