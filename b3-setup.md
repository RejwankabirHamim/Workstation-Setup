### 1. Setup B3 backend

https://github.com/appscode-cloud/launchpad/tree/master/2021/gitea_setup

### 2. Setup Cluster UI

#### Install npm
do that in bash shell:
```shell
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
$ source ~/.bashrc
$ nvm install 18
$ nvm use 18
```
####  Run Cluster UI
```shell
$ cd $HOME/go/src/go.bytebuilders.dev/cluster-ui

$ # install dependencies
$ npm i
$ # run Cluster UI
$ npm run serve
```

### 3. Setup platform UI

```azure
npm i && npm run serve
```

