# Peter's ESPHome repo

## Install ESPHome environment

See https://esphome.io/guides/installing_esphome

## Compile and install

```
esphome run <yaml file>
```

## Compile and install on a specific device

```
esphome run <yaml file> --device <ip address>
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

## Relevant projects

The code is based on the following GitHub projects:

* https://github.com/AzonInc/Doorman
* https://github.com/wichers/esphome-comfoair
* https://github.com/julianpas/esphome-comfoair
* https://github.com/esphome/bluetooth-proxies
