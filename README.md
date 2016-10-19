# LDU
A Lightweight Log-based Deferred Update for Linux Kernel Scalability

we introduce a lightweight log-based deferred update
method, combining the log-based concepts in the distributed systems and the
minimal hardware-based synchronization in the shared memory systems.
The main contributions of the proposed method are:(1) we propose a lightweight
log-based deferred update method, which can eliminate synchronized time-stamp counters that limits the performance scalability;and 
(2) we implemented the proposed method in the Linux 4.5-rc6 kernel
for two representative data structures (anonymous reverse mapping and 
file mapping) and evaluated the performance improvement due to our
proposed novel light weight update method. 
Our evaluation study showed that application of our method could
achieve from 1.5x through 2.7x performance improvements in 120 core
systems.


# Software

*kernel

LDU(global queue) : 
<pre>git clone https://github.com/linux-ldu/scalablelinux -b v4.5-rc6-IPDPS2017-anon_LDU_P-file_LDU_P</pre>

LDU(per-core queue) :

Harris : 


*benchmark


