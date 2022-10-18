# gpm

## Getting Started
go build main.go
./main 
go tool pprof –text /path/to/yourbinary /var/path/to/cpu.pprof
go tool pprof –pdf /path/to/yourbinary /var/path/to/cpu.pprof > cpu.pdf


## NOTE




go test -bench . -cpuprofile=cpu.prof
go test -bench . -memprofile=./mem.prof

