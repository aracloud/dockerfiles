FROM library/alpine:latest

RUN apk add --update \
	openssh-client \
	tar \
	curl \
	&& curl -kL https://github.com/coreos/fleet/releases/download/v0.11.5/fleet-v0.11.5-linux-amd64.tar.gz | tar -xvz --strip-components=1 -C /bin

WORKDIR /root/
	
ENTRYPOINT ["fleetctl"]
