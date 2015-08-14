FROM ubuntu:latest

RUN apt-get update \
	&& apt-get install -y \
		curl \
		usbutils \
		openjdk-7-jre \
	&& dpkg --add-architecture i386 \
    	&& apt-get -y install \
		libc6:i386 \
		libstdc++6:i386 \
	&& apt-get clean \
	&& curl -sSL http://dl.google.com/android/android-sdk_r24.1.2-linux.tgz | tar -C /usr/local/ -xvz

RUN echo y | /usr/local/android-sdk-linux/tools/android update sdk --filter platform-tools --no-ui --force
