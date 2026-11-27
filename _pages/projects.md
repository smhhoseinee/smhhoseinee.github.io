---
permalink: /projects/
title: "Projects"
author_profile: true
---

My research is on the [home page](/) and the [publications](/publications/) page. These are course and personal projects.

## Graduate course projects

- **TCP Nice congestion control** as a Linux kernel module in C, for CSCI 7000 Advanced Network Protocols at CU Boulder (Spring 2025). It adds TCP Nice's delay-based backoff to TCP Vegas. When more than 20% of a window's packets see high delay, it halves the congestion window. I compared it against Cubic, Reno, and Vegas. [GitHub](https://github.com/smhhoseinee/nice)
- **CUDA kernels for PyTorch** on an NVIDIA T4 GPU, for CSCI 7000 Systems for Machine Learning at CU Boulder (Fall 2025). I wrote a sepia-filter kernel, one thread per pixel, and compiled it into PyTorch with load_inline. It took 146 ms including copies to and from the GPU, versus 3.13 s in pure Python. A tiled shared-memory matrix multiply, adapted to non-square matrices, took 1.98 s at 8192×8192, versus 2.77 s for the naive kernel.
- **GPU timing and profiling in PyTorch**, for CSCI 7000 Systems for Machine Learning at CU Boulder (Fall 2025). Timed torch.square on a 20000×20000 matrix on a T4 GPU and traced it with torch.profiler. A plain Python timer read 0.011 ms because it caught only the kernel launch. The profiler measured 13.4 to 13.9 ms of GPU time per call.
- **Distribution shift in CNNs**, for CSCI 5922 Neural Networks and Deep Learning at CU Boulder (Spring 2025). A PyTorch pipeline trains LeNet, AlexNet, and ResNet-18 on CIFAR-10 with FP16 mixed precision, then tests them on CIFAR-10.2. Accuracy on CIFAR-10.2 was 11.58 to 14.38 points lower. ResNet-18 went from 90.08% to 78.5%.
- **Neural network training without autograd**, for CSCI 5922 Neural Networks and Deep Learning at CU Boulder (Spring 2025). I wrote the forward pass, backward pass, softmax, cross-entropy loss, and SGD updates of a multilayer perceptron by hand in PyTorch tensor operations. A sweep on MNIST compared 12 configurations of depth, width, and activation function.
- **Checkpoint-as-a-Service for LLM training**, for CSCI 5253 Datacenter Scale Computing at CU Boulder (Spring 2026). Four GCP clients write training checkpoints through NGINX to a 4-node MinIO cluster. A control plane turns client compression on and off from MinIO CPU load, and reweights NGINX from each node's disk write rate. In a disk-stress test, I/O-aware routing cut average upload time 10.4%.
- **Fault-tolerant distributed lock manager** in Python and gRPC, for the Distributed Systems course at the University of Edinburgh (Fall 2024). I built client retries, duplicate-request detection, lock timeouts, and server state recovery.

## Systems and networking

- **Network diagnostics tool** in C using raw sockets: port scan, ping, traceroute, and ARP host discovery. [GitHub](https://github.com/smhhoseinee/network-tool-port-scan-ping-tracroute-arp-discovery)
- **Multithreaded search engine** in Java, compared across five modes: single thread, threads without locks, mutex, semaphore, and a trie guarded by semaphores. A joint Operating Systems course project. [GitHub](https://github.com/smhhoseinee/multi_thread_search_engine)
- **Real-time scheduling simulator** in Java for a sample restaurant, comparing Earliest Deadline First, Rate Monotonic, and Least Laxity First. [GitHub](https://github.com/smhhoseinee/os_project_3_scheduling_for_restaurant)

## Parallel computing

- **Parallel genetic algorithm** for function optimization, parallelized with OpenMP in C++. [GitHub](https://github.com/smhhoseinee/genetic_algorithm_parallel_using_openmp)

## Infrastructure

- **Cloud computing system** set up and deployed for the ProCL application. [GitHub](https://github.com/smhhoseinee/ProCL-Application-setting-up-and-implementation-for-a-cloud-computing-system)
- **Monitoring stack** with Prometheus, Grafana, and Alertmanager configuration. [GitHub](https://github.com/smhhoseinee/Docker-Compose-Prometheus-and-Grafana)

## Theory of computation

- **Regular grammar to finite automaton converter** in Java. [GitHub](https://github.com/smhhoseinee/Regular_Grammar_To_FA_Converter)
