## Prerequisites

Anmain CLI is a fork of BHP.
You will need Window or Linux. Use a virtual machine if you have a Mac. Ubuntu 14 and 16 are supported. Ubuntu 17 is not supported.

Install [.NET Core](https://www.microsoft.com/net/download/core).

On Linux, install the LevelDB and SQLite3 dev packages. E.g. on Ubuntu:

```sh
Ubuntu:
sudo apt-get install libleveldb-dev sqlite3 libsqlite3-dev libunwind8-dev

Centos:
sudo yum install leveldb-devel sqlite-devel
```

On Windows, use the [Bhp version of LevelDB](https://github.com/BhpAlpha/bhp-leveldb).

## Run BHP-CLI on Linux
It is recommended to install tmux on Linux.
tmux is a terminal multiplexer. It lets you switch easily between several programs in one terminal, 
detach them (they keep running in the background) and reattach them to a different terminal. And do a lot more 

```sh
ubuntu: sudo apt-get install tmux
centos: sudo yum install tmux
```

### Create a session

tmux new -s [Custom number]
```sh
tmux new -s 1
```

### Enter the last session

tmux a -t [Custom number]
```sh
tmux a -t 1
``` 


## Download release binaries

Download and unzip [latest release](https://github.com/anmaichain/amc-cli/releases).

```sh
dotnet bhp-cli.dll
```
## Download plugins release binaries
Move wallet rpc to rpcwallet plugin after v1.2.0.6

```sh
Download the same version and unzip [latest release](https://github.com/BhpAlpha/bhp-plugins/releases).
```
 

```sh
cd bhp-cli
dotnet restore
dotnet publish -c Release
```
In order to run, you need .NET Core. Download the SDK [binary](https://www.microsoft.com/net/download/linux).

## Logging

To enable logs in bhp-cli, you need to add the ApplicationLogs plugin. Please check [here](https://github.com/BhpAlpha/bhp-plugins) for more information.
