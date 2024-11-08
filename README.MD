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
change proxy: go env -w GOPROXY=https://goproxy.cn,direct
```
### 1.3 Get Docker Ready
```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt update
sudo apt install docker-ce
sudo usermod -aG docker $USER
sudo apt remove docker-ce
sudo apt purge docker-ce
sudo rm -rf /var/lib/docker
```
### 1.5 Get Minikube Ready
```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64
```
### 1.6 Get Kubebuilder Ready
```
# download kubebuilder and install locally.
curl -L -o kubebuilder "https://go.kubebuilder.io/dl/latest/$(go env GOOS)/$(go env GOARCH)"
chmod +x kubebuilder && sudo mv kubebuilder /usr/local/bin/
https://kubebuilder.io/quick-start
```
