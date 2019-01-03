# Overview
AI Workers are computing resource providers in orion cloud. They rent out their GPU computing power on orion to provide support to compute-intensive workloads for platform users.

By simply running a few commands, individual machine with GPU may download and install client package, join orion network as an AI worker which allows them to be listed on developer dashboard. Such hosting allows automatically receiving tasks from orion task pool, and receive rewards upon successful computing.

# latest version
The latest version is v0.1.1

# update history
2018-11-16 |  0.0.0  
-initial version of ai worker for Orion platform

2018-11-22 |  0.0.1  
-Add UTC timestamp in worker terminal prompt

-Resolve and specify hardware recognition error

2018-12-11 |  0.1.1

-Added task script running Traceback in execution log

-Performance tested for AI worker network connection


# System Prerequisite #

**Must satisfy these minimum requirements to be eligible for an AI worker**
- Ubuntu 16.04 LTS.
- Installation of python 3.
- Nvidia CUDA-capable GPU(GeForce GTX 1060 6GB and up).
- Installation of CUDA (version>=9.0) , Nvidia-driver>=384.81
- Additional packages/libraries are not needed.

# Step-by-step guideline #

Please check : https://orioncloud.io/ai-workers.html#step-by-step
