# Melon Survival Server / Generic Minecraft Server Creator for Docker

## Setup

1. Clone the repository
2. Adjust the compose.yaml file to your needs
3. Use the included mod manager to download mods to the mods folder
4. Run `docker compose up -d`
5. Open the Minecraft server

## Adding custom world

1. Allow the server to start and create a world
2. Locate the volume that was generated for the world
3. Locate the world you want to copy
4. Copy the world to the volume with the following command: `docker cp <world_path_local> <container_id>:/data/world`
5. Change permissions with: `docker exec -it <container_id> chown -R minecraft:minecraft /data/world`
6. Restart the server
