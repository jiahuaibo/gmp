# gpm

## Getting Started
go build main.go
./main -cpu
go tool pprof cpu.pprof
top3
list main.logicCode
exit

go tool pprof main cpu.pprof
web

## NOTE
flat：当前函数占用CPU的耗时
flat：:当前函数占用CPU的耗时百分比 
sun%：函数占用CPU的耗时累计百分比 
cum：当前函数加上调用当前函数的函数占用CPU的总耗时 
cum%：当前函数加上调用当前函数的函数占用CPU的总耗时百分比 最后一列：函数名称

runtime/pprof：采集工具型应用运行数据进行分析 
net/http/pprof：采集服务型应用运行时数据进行分析 pprof开启后，每隔一段时间（10ms）就会收集下当前的堆栈信息，获取格格函数占用的CPU以及内存资源；最后通过对这些采样数据进行分析，形成一个性能分析报告。

每个框代表一个函数，理论上框的越大表示占用的CPU资源越多。 方框之间的线条代表函数之间的调用关系。 线条上的数字表示函数调用的次数。 方框中的第一行数字表示当前函数占用CPU的百分比，第二行数字表示当前函数累计占用CPU的百分比。

