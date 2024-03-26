# CSAPP_Labs
This repo is to record my work in CSAPP.

# Environment Setting
The labs are implemented on my Apple Macbook Air M1 laptop.
- Darwin 23.2.0 
- Darwin Kernel Version 23.2.0: Wed Nov 15 21:53:34 PST 2023
- root:xnu-10002.61.3~2/RELEASE_ARM64_T8103 arm64

However, since the lab environment should be a X86 architecture, I have to build a virtual environment on my ARM machine. I turn to Docker for help and find an already set environment: `docker pull xieguochao/csapp`. Set the mount directory, run the container and all is done. More information you may need: [Docker](https://www.docker.com/get-started/), [CSAPP labs](https://csapp.cs.cmu.edu/3e/labs.html).
