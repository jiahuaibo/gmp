# gpm

## Getting Started
go build main.go
./main
go tool pprof -seconds 10 http://localhost:9876/debug/pprof/profile
go tool pprof -http=:8081 ~/pprof/pprof.samples.cpu.004.pb.gz

优化顺序
LocalTz_1
doSomething_2
doSomething_3