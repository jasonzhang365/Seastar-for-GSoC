# Seastar-for-GSoC
## TCP BBR implementaion in Seastar

### Have done

- [x] User-defined command line. Making tcp congestion control algorithm configurable. In our implementation phrase "**--tcp-congestion**" will be used to configure tcp congestion control algorithm.
 
- [x] A high resolution timer. I just reuse the code in **core/lowres_clock.hh** to develop my timer in **microsecond granularity**. 

- [x] TCP BBR congestion window adjustment algorithm. Developing the basic TCP BBR state machine, and congestion window adjustment algorithm in Seastar.

### TODO LIST

- [ ] Accurate packet pacing. To implement TCP BBR, we should not only control the adjustment of congestion window, but also directly control the rate of packet pacing in layer 2.
 
- [ ] Separated BBR module. I will abstract tcp as a basic class, and make various tcp congestion control algorithms as tcp derived classes. In this way, we can easily develop multiple tcp congestion algorithm modules in seperated files.
 
- [ ] Comprehensive tests and evaluations.
