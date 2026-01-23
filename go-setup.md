# Go

## Install Go

To install Go, run the following command:

```console
go_version=1.25.5
cd ~/Downloads
sudo apt-get update
sudo apt-get install -y build-essential git curl wget
wget https://go.dev/dl/go${go_version}.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go${go_version}.linux-amd64.tar.gz
sudo chown -R $(id -u):$(id -g) /usr/local/go
rm go${go_version}.linux-amd64.tar.gz
```

Add go to your $PATH variable

```bash
mkdir $HOME/go
nano ~/.bashrc
export GOPATH=$HOME/go
export PATH=$GOPATH/bin:/usr/local/go/bin:$PATH
source ~/.bashrc
go version
```

## Install Intellij GoLand IDE

install from app-center
