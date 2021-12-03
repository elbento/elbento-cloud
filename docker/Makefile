SHELL:=/bin/bash
ARCH=`dpkg --print-architecture`
RELEASE=`lsb_release -cs`
include .env

.PHONY: repo install

repo:
	curl -fsSL https://download.docker.com/linux/ubuntu/gpg | \
		sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

	echo \
      "deb [arch=$(ARCH) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
      $(RELEASE) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

install:
	sudo apt-get update && sudo apt-get install docker-ce docker-ce-cli containerd.io
