NAME = chrisl/elixir-dev-centos
VERSION = 0.1.1

.PHONY: all build test tag_latest release ssh

all: build

build:
	docker build -t $(NAME):$(VERSION) -f Dockerfile --rm .
