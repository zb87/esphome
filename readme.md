# Peter's ESPHome repo

## Install ESPHome environment

See https://esphome.io/guides/installing_esphome

## Compile and install

```
esphome run <yaml file>
```

## Monitor the logs

```
esphome logs <yaml file>
```

## Run esphome commands via docker

Replace the `esphome` in the command with the following:

```
docker run --rm --net=host -v "${PWD}":/config -it ghcr.io/esphome/esphome
```

## Install Home Assistant Lovelace UI for ComfoAir controller

1. Copy the `lovelace-comfoair` directory to the `www` directory of Home Assistant config directory
1. Home Assistant -> Settings -> Dashboards -> "..." button -> Resources
1. Add a JavaScript module resource with the path `/local/lovelace-comfoair/comfoair-card.js`
1. In Home Assistant dashboard page, add a card with the following config:

```
- type: custom:comfoair-card
  entity: <Entity ID starts with climate>
```

## Relevant projects

The code is based on the following GitHub projects:

* https://github.com/wichers/esphome-comfoair
* https://github.com/wichers/lovelace-comfoair
* https://github.com/julianpas/esphome-comfoair
* https://github.com/esphome/bluetooth-proxies
