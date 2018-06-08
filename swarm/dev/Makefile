.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/go-apollyon/go-apollyon/cmd/swarm
	go build -o bin/geth     github.com/go-apollyon/go-apollyon/cmd/geth
	go build -o bin/bootnode github.com/go-apollyon/go-apollyon/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/go-apollyon/go-apollyon/swarm/...
