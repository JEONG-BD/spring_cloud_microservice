IMAGE_NAME=service-discovery
CONTAINER_NAME=service-discovery
PORT=8761
NETWORK=cloud-test
build:
	docker build -t $(IMAGE_NAME) .

run:
	docker rm -f $(CONTAINER_NAME)
	docker run -d --rm -p $(PORT):$(PORT) --name $(CONTAINER_NAME) --network $(NETWORK)  $(IMAGE_NAME)

stop:
	docker stop $(CONTAINER_NAME)
	docker rm $(CONTAINER_NAME)

logs:
	docker logs -f $(CONTAINER_NAME)