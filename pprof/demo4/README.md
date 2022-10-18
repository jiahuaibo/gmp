# gpm

## Getting Started
go build main.go
wrk -c 400 -t 8 -d 3m http://localhost:9876/test
-c, –connections 跟服务器建立并保持的TCP连接数量 
-d, --duration 压测时间 
-t, --threads 使用多少个线程进行压测 

curl -sK -v http://localhost:9876/debug/pprof/heap > heap.out

wget -o trace.out http://localhost:9876/debug/pprof/trace?seconds=20


http://localhost:9876/debug/pprof/
