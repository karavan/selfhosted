```sh
#--------------------------------------------------------------------------------------------#
#                     ArchiveBox - Open-source self-hosted web archiving                     #
#--------------------------------------------------------------------------------------------#
mkdir archivebox && cd archivebox
# Feel free to edit the docker-compose.yml and add/remove services and/or change the ports.
curl -O 'https://raw.githubusercontent.com/ArchiveBox/ArchiveBox/master/docker-compose.yml'
docker-compose run archivebox init --setup
docker-compose up

# Fixes chromium singlefile capture on Arm devices
docker-compose exec archivebox ln -s /usr/bin/chromium /usr/bin/chromium-browser
```
