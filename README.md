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

Reference: https://blog.handsomesnail.com/list/1593757406.html, I'm sorry that this reference is in Chinese. If you need help with the environment setting after translate the reference website, please leave me an issue. 

More information you may need: [Docker](https://www.docker.com/get-started/), [CSAPP labs](https://csapp.cs.cmu.edu/3e/labs.html).