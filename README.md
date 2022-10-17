# gpm

## Getting Started
go run trace.go
go tool trace trace.out 


go build main.go 
GODEBUG=schedtrace=1000 ./main 
<!-- 
SCHED：调试信息输出标志字符串，代表本行是goroutine调度器的输出；
0ms：即从程序启动到输出这行日志的时间；
gomaxprocs:P的数量，本例有2个P,因为默认的P的属性是和cpu核心数量默认一致，当然也可以通过GOMAXPROCS来设置；
idleprocs:处于idle状态的P的数量；通过gomaxprocs和idleprocs的差值，我们就可知道执行go代码的P的数量；
threads:os threads/M的数量，包含scheduler使用的m数量，加上runtime自用的类似sysmon这样的thread的数量；
spinningthreads:处于自旋状态的os thread数量；
idlethread:处于idle状态的os thread的数量；
runqueue=0:Scheduler全局队列中G的数量；
[0 0]:分别为2个P的local queue中的G的数量。 
-->
