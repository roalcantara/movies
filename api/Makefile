BACKEND ?= $(OKTETO_NAME)

.PHONY: build
build:
	go build -o bin/$(BACKEND) cmd/$(BACKEND)/main.go

.PHONY: load-data
load-data:
	bin/$(BACKEND) load-data

.PHONY: start
start:
	bin/$(BACKEND)

.PHONY: debug
debug:
	dlv debug --headless --listen=:2345 --log --api-version=2 cmd/$(BACKEND)/main.go
