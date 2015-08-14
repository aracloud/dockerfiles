NAMESPACE := vpommier
REPO := $(notdir $(CURDIR))
VERSION ?= latest

.PHONY: all build package clean 

all: build package clean

build:
	@mkdir -p ./opt/coreos-ipxe-server/configs
	@mkdir -p ./opt/coreos-ipxe-server/images
	@mkdir -p ./opt/coreos-ipxe-server/profiles
	@mkdir -p ./opt/coreos-ipxe-server/sshkeys
	@mkdir -p ./bin
	@docker run --rm \
		-v "${PWD}/bin/":/tmp/build/ \
		golang:1.3.3 \
		/bin/sh -c "CGO_ENABLED=0 go get -v -a -ldflags '-s' github.com/kelseyhightower/coreos-ipxe-server; cp /go/bin/coreos-ipxe-server /tmp/build"
package:
	@tar -cvf rootfs.tar ./opt ./bin && \
		docker build -t $(NAMESPACE)/$(REPO):$(VERSION) .
clean:
	@rm -rf ./opt ./bin ./rootfs.tar	
