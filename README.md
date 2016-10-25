# LDU
A Lightweight Log-based Deferred Update for Linux Kernel Scalability

In highly parallel computing systems with many-cores, a few critical
factors cause performance bottlenecks severely limiting scalability.
The kernel data structures with high update rate naturally cause 
performance bottlenecks due to very frequent locking of the data structures. 
There have been research on log-based synchronizations with time-stamps
that have achieved significant level of performance and scalability 
improvements. However, sequential merging operations of the logs with 
time-stamps pose another sources of scalability degradation.

To overcome the scalability degradation problem, we introduce a lightweight log-based deferred update
method, combining the log-based concepts in the distributed systems and the
minimal hardware-based synchronization in the shared memory systems.
The main contributions of the proposed method are:(1) we propose a lightweight
log-based deferred update method, which can eliminate synchronized time-stamp counters that limits the performance scalability;and (2) we implemented the proposed method in the Linux 4.5-rc6 kernel
for two representative data structures (anonymous reverse mapping and 
file mapping) and evaluated the performance improvement due to our
proposed novel light weight update method. 
Our evaluation study showed that application of our method could
achieve from 1.5x through 2.7x performance improvements in 120 core
systems.

# Software

## Modified kernel : https://github.com/manycore-ldu/linux

LDU(global queue) : 
<pre>git clone https://github.com/manycore-ldu/linux -b v4.5-rc6-ldu-global-queue</pre>
LDU(per-core queue) :
<pre>git clone https://github.com/manycore-ldu/linux -b v4.5-rc6-ldu-per-core-queue</pre>
Harris : 
<pre>git clone https://github.com/manycore-ldu/linux -b v4.5-rc6-harris</pre>

**anonymous mapping : mm/rmap.c

**file mapping : mm/mmap.c

## benchmark : https://github.com/manycore-ldu/benchmark


