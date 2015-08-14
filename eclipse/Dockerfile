FROM fedora:21

RUN yum install -y \
	java-1.8.0-openjdk \
	tar \
	gtk2 \
	&& yum clean all

RUN curl -sSL http://eclipse.ialto.com/technology/epp/downloads/release/luna/SR1a/eclipse-java-luna-SR1a-linux-gtk-x86_64.tar.gz \
	| tar -C /usr/local/ -xvz

ENTRYPOINT ["/usr/local/eclipse/eclipse"]
