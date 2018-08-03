build:
	go build -ldflags "-X main.version=$(TAG)" -o example .

pack: build
	docker build -t buckleywdavid/producer-consumer:$(TAG) 
