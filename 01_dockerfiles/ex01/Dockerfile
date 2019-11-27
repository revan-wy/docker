FROM debian

WORKDIR /teamspeak

EXPOSE 9987/udp 30033/tcp 10011/tcp 41144/tcp

ENV TS3SERVER_LICENSE="accept"

RUN apt update --yes && \
	apt upgrade --yes && \
	apt install wget --yes && \
	apt install bzip2 --yes && \
	wget https://files.teamspeak-services.com/releases/server/3.10.2/teamspeak3-server_linux_amd64-3.10.2.tar.bz2 && \
	tar xfv teamspeak3-server_linux_amd64-3.10.2.tar.bz2

WORKDIR /teamspeak/teamspeak3-server_linux_amd64

ENTRYPOINT sh ts3server_minimal_runscript.sh 

#build it
#docker build --tag ex01 ./

# run it
# docker run --interactive --tty --rm -p 9987:9987/udp -p 30033:30033/tcp -p 10011:10011/tcp -p 41144:41144/tcp ex01

