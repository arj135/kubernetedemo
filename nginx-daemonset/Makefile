# Makefile for Nginx DaemonSet project

.PHONY: build push deploy clean

IMAGE_NAME = nginx-daemonset
TAG = latest

build:
	docker build -t $(IMAGE_NAME):$(TAG) .

push:
	docker push $(IMAGE_NAME):$(TAG)

deploy:
	kubectl apply -k k8s/

clean:
	docker rmi $(IMAGE_NAME):$(TAG)