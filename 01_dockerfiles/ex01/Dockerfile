FROM debian
RUN apt-get update && apt-get upgrade -y
ADD http://dl.4players.de/ts/releases/3.0.11.2/teamspeak3-server_linux-amd64-3.0.11.2.tar.gz ./
RUN tar -xvzf teamspeak3-server_linux-amd64-3.0.11.2.tar.gz
EXPOSE 9987/udp
EXPOSE 10011
EXPOSE 30033
CMD ["sh", "teamspeak3-server_linux-amd64/ts3server_minimal_runscript.sh"]
