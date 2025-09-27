# mcsm-remastered

Minecraft server management script for FreeBSD.

## 1. Install

```sh
$ pkg install git tmux curl jq
## Make sure to install the correct java version: openjdk<java_version> eg: openjdk21
$ git clone git@github.com:ChickenMst/mcsm-remastered.git mcsm-remastered
$ cd mcsm-remastered/build/freebsd
$ make install
```

## 2. Create & Update Server

```sh
$ mcsm create SERVERNAME
$ mcsm update SERVERNAME VERSION
## Either latest or the version number eg: 1.21.2
```
or
```sh
$ mcsm create SERVERNAME VERSION
```


## Start Server

```sh
$ mcsm start SERVERNAME
Wakeup SERVERNAME.
```


## Status

```sh
$ mcsm status
   PID  Servername
 70635  SERVERNAME
```


## Server console

```sh
$ mcsm console SERVERNAME
```

exit console : Ctrl+b => d


## Stop Server

```sh
$ mcsm stop SERVERNAME
Stopping 'SERVERNAME' please wait for about 30 seconds.
```

## Stop All Servers

```sh
$ mcsm stop all
```


## Auto start & Auto stop

```sh
$ service mcsm enable
## The service runs as root, so please read the posible consequences provided by papermc
```
