# Smartphone Test Farm using Docker on Raspberry Pi

This docker-compose config contains open stf, rethinkdb and adb.

In order to use it:

- Install Docker and [docker-compose](https://docs.docker.com/compose/install/)
- Open the docker-compose.yml file and edit the ip address there, entering your server's ip address instead
- Leave the docker-compose.yml file inside your home directory (/home/pi)
- Copy the docker-infra.service file from the systemd directory to /etc/systemd/system
- Reload the daemons: sudo systemctl daemon-reload
- Enable the service: sudo systemctl enable docker-infra
- Start everything: sudo systemctl start docker-infra

After everything is loaded, your server will be available on http://< the ip address you configured >:7100
