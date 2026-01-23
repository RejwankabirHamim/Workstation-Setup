## Install git

```bash
sudo apt-get install git git-gui
```
### Configure git

```bash
git config --global user.name RejwankabirHamim
git config --global user.email <your-email>
```
### Git ignore .DS_Store  (  for mac )

- https://0xmachos.com/2020-01-22-Eradicating-.DS_Store-From-Git/

```bash
echo .DS_Store > ~/.gitignore

git config --global core.excludesfile ~/.gitignore
```
