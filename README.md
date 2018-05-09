# swissarmyknife-minecraft-server

Minecraft server container with a :purse: :briefcase: :handbag: collection of ⛑️  essential plugins and :beginner: opinionated configurations:

* https://luckperms.github.io
* https://nucleuspowered.org

Typically used with [s2i-minecraft-server](https://github.com/vorburger/s2i-minecraft-server/) - but doesn't have to be.


## Local Build

    s2i build --copy . s2i-minecraft-server swissarmyknife-minecraft-server

    docker run -it --rm -p 25565:25565 swissarmyknife-minecraft-server

    > /lp import ../setup/luckperms.cmds
    > /lp user <YOU> parent add groot
    > /nucleus setupperms ADMIN groot
    > /nucleus setupperms MOD boss
    > /nucleus setupperms USER assistant

## OpenShift

    oc new-build s2i-minecraft-server~https://github.com/OASIS-learn-study/swissarmyknife-minecraft-server.git

You now have to be creative to be able to do the initial (above) `/lp` commands! ;-)

Use e.g. the maintenance-minecraft-server and mount the production volume into it, `oc rsh` into it,
manually run the `mkdir` and `ln` from the `.s2i/bin/run`, then start the server in the foreground
using `/usr/local/s2i/run` and on that console run above.
