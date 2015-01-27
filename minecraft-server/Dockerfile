FROM duncsmith/jdk7

ENV VERSION 1.8

EXPOSE 25565

VOLUME ["/data"]
VOLUME ["/data/world"]

ADD server.properties /data/server.properties
ADD ops.json /data/ops.json
ADD whitelist.json /data/whitelist.json
ADD eula.txt /data/eula.txt
ADD https://s3.amazonaws.com/Minecraft.Download/versions/$VERSION/minecraft_server.$VERSION.jar /data/minecraft_server.jar

WORKDIR /data

CMD ["-Xmx1024M","-Xms1024M","-jar","minecraft_server.jar","nogui"]
ENTRYPOINT ["/usr/bin/java"]
