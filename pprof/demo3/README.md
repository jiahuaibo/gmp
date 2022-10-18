# gpm

## Getting Started
go build main.go
wrk -c 400 -t 8 -d 3m http://localhost:9876/test
-c, –connections 跟服务器建立并保持的TCP连接数量 
-d, --duration 压测时间 
-t, --threads 使用多少个线程进行压测 
这时我们打开http://localhost:9876/debug/pprof
打开链接http://localhost:9876/debug/pprof/profile稍后片刻，可以下载到文件profile。
go tool pprof main profile
top