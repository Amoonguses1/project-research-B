IMAGE_NAME=gpu_pytorch_gan
CONTAINER_NAME=gpu_pytorch_gan
FORCE_RM=true

stop:
	docker stop $(CONTAINER_NAME)

build:
	docker build \
		-f docker/Dockerfile \
		-t $(IMAGE_NAME) \
		--no-cache \
		--force-rm=$(FORCE_RM) \
		.
run:
	docker run --rm -it  --gpus 1 -v \
	$(pwd):/work gpu_pytorch_gan:latest

exec:
	docker exec \
	  -it \
  	$(CONTAINER_NAME) bash