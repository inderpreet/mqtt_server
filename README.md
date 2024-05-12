# MQTT Broker Docker Image and config

This repo contains the docker compoose file and other tit-bits to start a broker.

## Start the broker

```
docker compose up -d
```

## Adding a new user

Run the following command once the docker image is up.

```sh
docker compose exec mosquitto sh
```

Once you get a shell, use this command to add a new user

```sh
mosquitto_passwd -c /mosquitto/config/pwfile <USERNAME>
```

Restart with
```sh
docker compose restart mosquitto
```
