# mcsm-remastered

Minecraft server management script for FreeBSD.

## 1. INSTALL

```sh
$ pkg install git tmux curl jq
## Make sure to install the correct java version: openjdk<java_version> eg: openjdk21
$ git clone git@github.com:ChickenMst/mcsm-remastered.git mcsm-remastered
$ cd mcsm-remastered/build/freebsd
$ make install
```

## 2. Update server program

```sh
$ mcsm update SERVERNAME 1.19
```


## Create & Start

```sh
$ mcsm create SERVERNAME
Created server dir '/var/games/minecraft/servers/SERVERNAME'.
/var/games/minecraft/servers/SERVERNAME/mcsm.conf
$ mcsm start MYWORLD
Wakeup SERVERNAME.
```


## Status

```sh
$ mcsm status
   PID  Servername
 70635  MYWORLD
```


## Server console

```sh
$ mcsm console SERVERNAME
```

exit console : Ctrl+b => d


## Stop

```sh
$ mcsm stop SERVERNAME
Stopping 'SERVERNAME' please wait for about 30 seconds.
```

## Stop all

```sh
$ mcsm stop all
```


## Auto start & Auto stop

```sh
$ service mcsm enable
## 
```
