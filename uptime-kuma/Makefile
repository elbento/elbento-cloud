SHELL:=/bin/bash
include .env

.PHONY: install up down

install:
	# Update your npm to the latest version
	npm install npm -g

	git clone https://github.com/louislam/uptime-kuma.git
	cd uptime-kuma
	npm run setup

	# Option 1. Try it
	#node server/server.js

	# (Recommended) Option 2. Run in background using PM2
	# Install PM2 if you don't have it: npm install pm2 -g
	#pm2 start server/server.js --name uptime-kuma

up:
	docker compose up -d

down:
	docker compose down

logs:
	docker compose logs -f
