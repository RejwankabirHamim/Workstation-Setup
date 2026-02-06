### 1. Download and Install Brew
To begin, download the Homebrew setup script for Ubuntu and execute it by running the command below:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

```aiignore
(echo; echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"') >> $HOME/.bashrc
```

```aiignore
eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
```


### 2. Install the Buf CLI

```aiignore
brew install bufbuild/buf/buf
```

### 3. Install antigravity

1. Add the repository to sources.list.d

```aiignore
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://us-central1-apt.pkg.dev/doc/repo-signing-key.gpg | \
  sudo gpg --dearmor --yes -o /etc/apt/keyrings/antigravity-repo-key.gpg
echo "deb [signed-by=/etc/apt/keyrings/antigravity-repo-key.gpg] https://us-central1-apt.pkg.dev/projects/antigravity-auto-updater-dev/ antigravity-debian main" | \
  sudo tee /etc/apt/sources.list.d/antigravity.list > /dev/null
```

2. Update the package cache
```aiignore
sudo apt update
```
3. Install antigravity
```aiignore
sudo apt install antigravity
```  
### 4. Install goimports
```aiignore
go install golang.org/x/tools/cmd/goimports@latest
```

### 4. Install pgadmin4

If you prefer a self-contained package (desktop + web in one):
```aiignore
sudo apt update
sudo apt install snapd
sudo snap install pgadmin4
```

### 5 . Install helm

```aiignore
brew install helm
```

### 6. Install clusterctl

```aiignore
curl -L https://github.com/kubernetes-sigs/cluster-api/releases/download/v1.12.2/clusterctl-linux-amd64 -o clusterctl
sudo install -o root -g root -m 0755 clusterctl /usr/local/bin/clusterctl
```

### 7. Setup tailscale

```aiignore
curl -fsSL https://tailscale.com/install.sh | sh

sudo tailscale up --login-server http://172.105.61.52:5050 --authkey 8d0778e8aeda2f099406ff6e78900a0ea6a1d64fc051991c --accept-routes
```

### 8. Install etcd

Update homebrew:
```aiignore
brew update
```

Install etcd:

```aiignore
brew install etcd
```

Verify install

```azure
etcd --version
```
