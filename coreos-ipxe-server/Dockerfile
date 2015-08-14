FROM library/scratch:latest

ADD rootfs.tar /

ENV COREOS_IPXE_SERVER_DATA_DIR /opt/coreos-ipxe-server
ENV COREOS_IPXE_SERVER_BASE_URL coreos.ipxe.example.com:4777
ENV COREOS_IPXE_SERVER_LISTEN_ADDR 0.0.0.0:4777

EXPOSE 4777

CMD ["/bin/coreos-ipxe-server"]
