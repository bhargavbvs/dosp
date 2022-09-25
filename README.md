## COP5615 - Distrbuted Operating System Principles
## Project 1

| Member | UFID |
| ------ | ------ |
| Venkata Sai Bhargav Bathini | 12796591 |
| Srikar Chowdary Kantamani | 69473991 |

## Overview
The goal of this project is to build a mining system that can find strings which when encoded using SHA-256 hashing function contains "n" number of leading zeroes where n is specified as input. This system as the value of n grows becomes computationally intensive and this is efficiently handled by using Actor Model in Erlang where the work or process is scaled across various threads. This increases the utilization of he CPU and thus efficiency of the mining system.

## Execution Steps
> `erl -name <username>@<IPAddress>` #Creating a node
> 
>  `c(mining.erl).` #Compile Erl file
>  
>  `mining.begin_erlserver().` #Starting a server in the node
>  
>  `mining:calculator('<username>@<IPAddress>',<workunits>).` #Running the Miner

#### Variables
     username: Your sytems username
     IPAddress: Your systems Ip address
     worknits: Desired number of workers
  
## Size of the Work Unit

| Actors | CPU Time(ms) | Real Time(ms) | Ratio( CPU time / Realtime) |
| ------ | ------ | ------ | ------ |
| 5 | 596955 | 302105 | 1.97598 |
| 100 | 1474999 | 201937 | 7.30425 |
| 1000 | 18569145 | 223372 | 8.31216 |
#### Specification:
Hashing performed on a string size of 500 and finding hashes with 4 leading zeroes.

## Observation
From our test we found our code works best with 1000 actors with CPU to Real time ratio of 8.31216. So we wll further perform tests using 1000 actors on a string size of 150 to find a coin with highest number of leading zeroes.
## Results (Input: 4)
![Executuon](https://user-images.githubusercontent.com/61014960/192125326-f2a50ecc-6b4b-449b-b933-a0f771902cc9.jpeg)

![output](https://user-images.githubusercontent.com/61014960/192125331-0a0be2d2-4dfc-439c-9075-700fbc536f3b.jpeg)

#### Running Time stats
CPU time: 18569145 ms
Real Time: 223372
Ratio( CPU to Real time) : 8.31216

## Coins with most number of zeroes
We found a bitcoin with 7 leading zeroes with 1000 workers on a string of length 150.
![max_number_of_zeroes](https://user-images.githubusercontent.com/61014960/192126074-fda5a253-b766-44d9-94d6-0ab0398552dc.jpeg)

 ## Largest number of working machines

