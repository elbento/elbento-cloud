SHELL:=/bin/bash
include .env

.PHONY: install up down

install:
	bash <(curl -Ss https://my-netdata.io/kickstart.sh)

up:
	docker compose up -d

down:
	docker compose down

logs:
	docker compose logs -f
