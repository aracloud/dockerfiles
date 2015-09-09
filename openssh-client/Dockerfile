FROM library/alpine:latest

RUN apk add --update openssh-client

RUN mkdir -p /sshagent

VOLUME /sshagent 

CMD ["ssh"]
