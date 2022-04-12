# bug fixing...

# 将内网设备通过公网服务器转发流量实现穿透
local<--->cloud<--->remote
## Linux
#### 远程客户端
```cmd
git clone https://github.com/Golds-l/goproxy.git
cd goproxy/
go build -o remoteClient client.go
./remoteClient -cS x.x.x.x -cSP xxx -lH x.x.x.x -lHP xxx
```
#### 公网服务端
```cmd
git clone https://github.com/Golds-l/goproxy.git
cd goproxy/
go build -o serverCloud server.go
./serverCloud -rP xxx -lP xxx
```
