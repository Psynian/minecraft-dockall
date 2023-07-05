# minecraft-dockall

Simple script to set up a cluster of Minecraft servers fronted by Bungeecord and Bedrock connect to let the widest range of devices play together.

***NOT WORKING YET COMING SOON***

Installs the following:
- DNS server/Bedrock connect server to allow Nintendo Switch to play
- Bungeecord server with GeyserMC plugin
- Bedrock server
- MariaDB SQL database
- three Minecraft java servers
- suite of admin tools

Instructions for Ubuntu

Setting up Docker environment (run as a non root user)
```
sudo apt update
sudo apt install docker docker-compose curl wget gh
sudo gpasswd -a $USER docker
```

Getting the repository
```
gh repo clone Psynian/minecraft-dockall
```

Run the initial setup script
```
chmod 755 setup.sh
./setup.sh
```

Bring up docker
```
docker-compose up
```
