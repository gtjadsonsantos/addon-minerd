TAG = latest
REPO = unicontrol/addon-minerd
NAME = addon-minerd

build:
	@docker build -t $(REPO):$(TAG) \
		--build-arg BUILD_FROM=ghcr.io/hassio-addons/debian-base/amd64:14.1.0 \
		--build-arg BUILD_ARCH=amd64 \
		--build-arg BUILD_DATE=$(date) \
		--build-arg BUILD_REPOSITORY=https://github.com/gtjadsonsantos/addon-minerd/tree/main/minerd \
		--build-arg BUILD_VERSION=1.0.0 .
			
	@docker tag $(REPO):$(TAG) unicontrol/$(NAME)
	
push: 
	@docker push $(REPO):$(TAG) 

release: build push