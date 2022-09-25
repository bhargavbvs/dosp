## COP5615 - Distrbuted Operating System Principles
### Project 1

| Member | UFID |
| ------ | ------ |
| Venkata Sai Bhargav Bathini | 12796591 |
| Srikar Chowdary Kantamani | 69473991 |

### Overview
The goal of this project is to build a mining system that can find strings which when encoded using SHA-256 hashing function contains "n" number of leading zeroes where n is specified as input. This system as the value of n grows becomes computationally intensive and this is efficiently handled by using Actor Model in Erlang where the work or process is scaled across various threads. This increases the utilization of he CPU and thus efficiency of the mining system.

### Size of the Work Unit

| Actors | CPU Time(ms) | Real Time(ms) | Ratio( CPU time / Realtime) |
| ------ | ------ | ------ | ------ |
| 5 | 596955 | 302105 | 1.97598 |
| 100 | 1474999 | 201937 | 7.30425 |
| 1000 |  |  |  |

### Observation

### Results (Input: 4)
