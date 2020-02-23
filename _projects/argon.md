---
title: "Argon RTOS"
---

Argon is a small embedded RTOS with clean C and C++ APIs for Arm Cortex-M-based microcontrollers.

It is designed to be a clean preemptive RTOS kernel with a C++ API. A plain C API upon which the C++
API is built is also available. It is primarily targeted at microcontrollers with Arm Cortex-M
processors. One of the key goals is for the source code to be highly readable, maintainable, and
well commented.

The kernel objects provided by Argon are:

- Thread
- Semaphore
- Mutex
- Queue
- Channel
- Timer
- Run Loop

Runloops enable very efficient use of threads, including waiting on multiple queues. Timers always
(and only) run on runloops instead of a dedicated timer thread. This lets you control the thread and
priority of timers.

Argon is open source software released with a BSD three-clause license.

The GitHub project is located at [https://github.com/flit/argon-rtos](https://github.com/flit/argon-rtos).



