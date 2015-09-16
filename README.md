# Katana (刀)
Katana is a fork of [PocketMine-MP](http://github.com/PocketMine/PocketMine-MP) designed for large-scale server networks. It focuses on providing the best possible performance through simplicity and only features essential to running a network.

### Features
- **Powerful chunk caching and processing system.**
    - Chunks are only encoded to be sent to the client once, freeing up many compute cycles
    - The results of chunk encoding are stored to and loaded from a disk cache or RAM
    - Lightweight process for sending chunks is easy to modify to fit your server's needs
- **Revamped console.**
    - Verbosity only when necessary
    - Colored and formatted console messages greatly improve readability
- **Production ready.**
    - Ability to disable all logging on player game servers reduces disk I/O
    - Future: Implement auto-updating system to make managing large deployments easy
    - Katana can redirect players when no slots are available or the server is lagging

### Warnings & Intentional Incompatibility
- Katana does not support leveldb.
- Katana does not use PocketMine's auto-updating or stats tracking systems.
- Katana will only generate empty chunks for regions of the world that are not set.
- Katana's default caching systems do not allow for worlds that are changed dynamically and saved (e.g. survival or player creative build worlds)
- Katana performs reduced physics calculations.
- Katana does not tick mob AIs.
- Katana does not support packet channels.
- Katana forces biome colors to be green. :rainbow:

### Design Philosophy
This server software was created and is maintained by William Teder and Ethan Kuehnel of Hydreon Corporation for the Lifeboat Server Network. We recognize that the functionality that is needed to run large minigame networks differs from that needed to run more vanilla servers. We hope that by removing unused features we can simplify core functions to make them easier to understand and maintain, while reducing overhead to improve performance. This is not software for everyone, this is software for our intended use. Hopefully you find it useful too.