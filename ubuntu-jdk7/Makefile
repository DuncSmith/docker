all: build

build:
	docker build -t duncsmith/jdk7 .

run:
	docker run -d --name="jdk7" duncsmith/jdk7

shell:
	docker run -i -t --name="jdk7" duncsmith/jdk7

start:
	docker start jdk7

stop:
	docker stop jdk7

clean: stop
	docker rm jdk7