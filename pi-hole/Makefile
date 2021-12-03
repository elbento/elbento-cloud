SHELL:=/bin/bash
include .env

.PHONY: install up down

install:
	curl -sSL https://install.pi-hole.net | bash

up:
	docker compose up -d

down:
	docker compose down
logs:
	docker compose logs -f
