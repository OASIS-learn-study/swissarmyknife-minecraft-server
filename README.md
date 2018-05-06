# swissarmyknife-minecraft-server

Minecraft server in a container with a collection of essential (Sponge) plugins and opinionated configurations.


## Local Build

    s2i build --copy . s2i-minecraft-server swissarmyknife-minecraft-server

    docker run --rm -p 25565:25565 swissarmyknife-minecraft-server
