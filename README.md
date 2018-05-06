# swissarmyknife-minecraft-server

Minecraft server container with a :purse: :briefcase: :handbag: collection of ⛑️ essential plugins and :beginner: opinionated configurations:

* https://luckperms.github.io
* https://nucleuspowered.org

Typically used with [s2i-minecraft-server](https://github.com/vorburger/s2i-minecraft-server/) - but doesn't have to be.


## Local Build

    s2i build --copy . s2i-minecraft-server swissarmyknife-minecraft-server

    docker run --rm -p 25565:25565 swissarmyknife-minecraft-server
