## 1 Preparation
### 1.1 Get Win10 Ready
`

`
### 1.2 Get Go Ready
```
wget https://go.dev/dl/go1.22.4.linux-amd64.tar.gz -P /usr/local
cd /usr/local && tar -zxvf go1.22.4.linux-amd64.tar.gz
add in .bashrc
export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export PATH=$PATH:/usr/local/go/bin
source ./bashrc
go version
```
