# LDU
A Lightweight Log-based Deferred Update for Linux Kernel Scalability

we introduce a lightweight log-based deferred update
method, combining the log-based concepts in the distributed systems and the
minimal hardware-based synchronization in the shared memory systems.

we implemented the proposed method in the Linux 4.5-rc6 kernel
for two representative data structures (anonymous reverse mapping and 
file mapping) and evaluated the performance improvement due to our
proposed novel light weight update method. 

Our evaluation study showed that application of our method could
achieve from 1.5x through 2.7x performance improvements in 120 core
systems.


# Software

## kernel : https://github.com/manycore-ldu/linux

LDU(global queue) : 
<pre>git clone https://github.com/manycore-ldu/linux -b v4.5-rc6-ldu-global-queue</pre>
LDU(per-core queue) :
<pre>git clone https://github.com/manycore-ldu/linux -b v4.5-rc6-ldu-per-core-queue</pre>
Harris : 
<pre>git clone https://github.com/manycore-ldu/linux -b v4.5-rc6-harris</pre>

*anonymous mapping : mm/rmap.c
*file mapping : mm/mmap.c

## benchmark : https://github.com/manycore-ldu/benchmark


