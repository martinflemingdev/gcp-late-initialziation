IMAGE_NAME=myapp
TAG=latest
BUILDER=buildah

.PHONY: build push run clean

# Build the container image using Buildah
build:
	$(BUILDER) bud -t $(IMAGE_NAME):$(TAG) .

# Push the image to a registry (optional)
push:
	$(BUILDER) push $(IMAGE_NAME):$(TAG) docker://your-registry.com/$(IMAGE_NAME):$(TAG)

# Run the container
run:
	podman run --rm $(IMAGE_NAME):$(TAG)

# Clean up any old images
clean:
	$(BUILDER) rmi $(IMAGE_NAME):$(TAG)
