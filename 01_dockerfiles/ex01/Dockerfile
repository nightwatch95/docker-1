FROM debian:latest

ENV TS3SERVER_LICENSE=accept
ARG VERSION=3.8.0

RUN apt-get update && \
	apt-get upgrade && \
	apt-get -y install wget bzip2 && \
	wget http://dl.4players.de/ts/releases/$VERSION/teamspeak3-server_linux_amd64-$VERSION.tar.bz2 && \
	tar -xvf teamspeak3-server_linux_amd64-$VERSION.tar.bz2
		
EXPOSE 9987/udp 30033 10011 

ENTRYPOINT ["sh", "./teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"]
