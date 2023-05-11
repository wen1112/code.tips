![image](https://github.com/wen1112/code.tips/assets/71487119/085e703b-f2a3-4e80-96a9-1236b58d7ff1)  


Command being timed: "bash marker.split.1.repeat10.sh"：表示被测量的命令是 "bash marker.split.1.repeat10.sh"。

User time (seconds): 1105.10：表示程序在用户空间（即应用程序层面）运行的时间，单位为秒。这个数值包括了应用程序在CPU上运行的时间，不包括操作系统和其他系统任务的运行时间。

System time (seconds): 33.75：表示程序在内核空间（即操作系统层面）运行的时间，单位为秒。这个数值反映了程序对系统资源的使用情况。

Percent of CPU this job got: 192%：表示程序使用的CPU时间占总CPU时间的百分比。如果这个值超过了100%，说明程序使用了多个CPU或者CPU时间片切换导致的CPU时间重复计算。

Elapsed (wall clock) time (h:mm:ss or m:ss): 9:52.00：表示程序从开始运行到结束的实际时间，包括了程序在CPU上运行的时间和等待CPU的时间。

Average shared text size (kbytes): 0：表示程序的代码段的大小，单位为KB。如果这个数值较大，说明程序代码比较复杂。

Average unshared data size (kbytes): 0：表示程序的非共享数据段（如堆和栈）的大小，单位为KB。这个数值反映了程序在内存中占用的空间。

Average stack size (kbytes): 0：表示程序的栈的大小，单位为KB。栈是一种内存分配方式，用于存储函数调用的参数、返回地址和局部变量等信息。

Average total size (kbytes): 0：表示程序占用的总内存大小，单位为KB。

Maximum resident set size (kbytes): 6689212：表示程序在运行过程中使用的最大物理内存大小，单位为KB。

Average resident set size (kbytes): 0：表示程序在运行过程中使用的平均物理内存大小，单位为KB。

Major (requiring I/O) page faults: 4：表示程序在运行过程中由于缺少已分配内存而需要进行I/O操作的数量。

Minor (reclaiming a frame) page faults: 377773：表示程序在运行过程中由于未分配内存而需要进行页面调度的数量。

Voluntary context switches: 131411：表示程序在运行过程中主动进行上下文切换的次数。

Involuntary context switches: 277081：表示程序在运行过程中被迫进行上下文切换的次数。

Swaps: 0：表示程序在运行过程中需要进行的交换操作的数量。

File system inputs: 文件系统读取次数，表示从文件系统中读取的字节数。它可以用来衡量应用程序的I/O负载。

File system outputs: 文件系统写入次数，表示向文件系统写入的字节数。它可以用来衡量应用程序的I/O负载。

Socket messages sent: 发送的套接字消息数，表示应用程序通过网络发送的消息数量。

Socket messages received: 接收的套接字消息数，表示应用程序通过网络接收的消息数量。

Signals delivered: 发送的信号数量，表示应用程序接收到的UNIX信号数量。

Page size (bytes): 页面大小（字节），表示系统用于虚拟内存管理的页面大小。

Exit status：命令的退出状态。通常，0 表示成功，非 0 表示失败。
