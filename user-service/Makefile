IMAGE_NAME=user-service
CONTAINER_NAME=user-service
PORT=60000
NETWORK=cloud-test
CONTAINER_NAME_2=user-service2
PORT2=60001

build:
	docker build -t $(IMAGE_NAME) .

run:
	docker rm -f $(CONTAINER_NAME)
	docker run -d --rm -p $(PORT):$(PORT) -e SERVER_PORT=$(PORT) --name $(CONTAINER_NAME) --network $(NETWORK) $(IMAGE_NAME)
run_2:
	docker rm -f $(CONTAINER_NAME_2)
	docker run -d --rm -p $(PORT2):$(PORT2) -e SERVER_PORT=$(PORT2) --name $(CONTAINER_NAME_2) --network $(NETWORK) $(IMAGE_NAME)
stop:
	docker stop $(CONTAINER_NAME)
	docker rm $(CONTAINER_NAME)

logs:
	docker logs -f $(CONTAINER_NAME)


