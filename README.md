# mlSys
ml Sys技术整理与分享


1 CUDA/TVM (软硬件加速相关）
2 Tensorflow/Pytorch/Ray(框架设计相关）
3 k8s/docker(云原生相关）



CUDA 

网格grid 线程块block 

网格启动等价于内核启动

线程块由SM （流式多处理器执行）通过线程束执行 每个线程束 32个线程 通过SIMT方式执行。

线程束在执行的时候分配了相同的指令。对于if else 可以通过线程数分化解决，牺牲其并行性。我们可以根据线程束防止其分化。（编译器会自动优化）



