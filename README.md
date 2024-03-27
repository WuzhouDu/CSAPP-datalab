# CSAPP_Labs
This repo is to record my work in CSAPP.

# Environment Setting
The labs are implemented on my Apple Macbook Air M1 laptop.
- Darwin 23.2.0 
- Darwin Kernel Version 23.2.0: Wed Nov 15 21:53:34 PST 2023
- root:xnu-10002.61.3~2/RELEASE_ARM64_T8103 arm64

However, since the lab environment should be a X86 architecture, I have to build a virtual environment on my ARM machine. I turn to Docker for help and found a Ubuntu environment: `docker pull ubuntu:18.04`. Set the mount directory, run the container. 
- update apt: `apt-get update`
- install sudo `apt-get install sudo`
- install c/c++ compile tool: `sudo apt-get install build-essential` `sudo apt-get install gcc-multilib`
- gdb: `sudo apt-get install gdb`

Reference: https://blog.handsomesnail.com/list/1593757406.html, I'm sorry that this reference is in Chinese. If you still need help with the environment setting after translating the reference website, please leave me an issue.

More information you may need: [Docker](https://www.docker.com/get-started/), [CSAPP labs](https://csapp.cs.cmu.edu/3e/labs.html).

# What I learn
## Datalab
> The datalab is about completing a series of functions with a restricted set of operators (I have to say that most of the restrictions are very artificial and well-crafted for the homework).

I learned a lot about bitwise operations, two's complement, and the machine-level representation of integer and floating-point numbers. Specifically, I am impressed by the following points:
1. exclusive or (^): 
   1. x ^ 0 has no meaning...
   2. x ^ 1 is the same as ~x
   3. x ^ x is 0. This can be used to verify the value of x, if you cannot use the equal sign. For example, if you want to verify that x is 0x12345678, you can use !!(x ^ 0x12345678).
2. Number representation:
   1. The $Tmin$ is a sepcial case when considering the two's complement. Its negative number is itself.
   2. I come to realize that why the two's complement number is designed as it is. The negative of a two's complement is ~x + 1, which is very convenient for the computer to calculate. Also, x + ~x + 1 will always lead to 0 (think about the binary level representation!).
   3. When implementing the `floatScale2` function, I understand that the gap between denormalized value and normalized value can be filled by just left shifting the fraction part. It's a very subtle design and **I recommend you to  finish this function** (despite the itimidating rate 4 difficulty!).