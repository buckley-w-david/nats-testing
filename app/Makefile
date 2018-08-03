TAG?=$(shell git rev-list HEAD --max-count=1 --abbrev-commit)
export TAG

build:
	go get -d 
	go build -ldflags "-X main.version=$(TAG)" -o bin/example .

pack: build
	docker build -t buckleywdavid/producer-consumer:$(TAG) 

upload: pack
	docker push buckleywdavid/producer-consumer:$(TAG)
	docker push buckleywdavid/producer-consumer:latest
