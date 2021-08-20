.PHONY: setup install dev

default: help

help:
					@echo "Usage:"
					@echo "  make setup      Step 1 - Creates the required shared docker volume for node_modules"
					@echo "  make install    Step 2 - Builds the required docker images and installs the node_modules"
					@echo "  make dev        Step 3 - Starts the container with the web application and runs it"

setup:
					docker volume create nodemodules
install:
					docker-compose -f docker-compose.builder.yml run --rm install
dev:
					docker-compose up