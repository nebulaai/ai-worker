
**[What is AI worker](#what-is-ai-worker)** | 
**[Prerequisites](#prerequisites)** |
**[Installation](#installation)** |
**[Release History](#release-history)** |
**[Getting Help](#getting-help)** | 
**[Licence](#licence)** |
**[Resources](#resources)** |  

# [Nebula AI Worker](https://github.com/nebulaai/ai-worker)

Official Orion AI worker software release.

## What is AI worker

**AI Workers** are computing resource providers in [orion cloud platform](https://orioncloud.io/). They execute AI tasks and receive NBAI as rewards. 
Individual GPU machine may download latest packages, install and join into Orion network. 
By simply running a few commands, AI tasks from Orion will be automatically dispatched to AI workers, you will be able to rent out your computing power for a real profit.     

## Prerequisites

Minimum system requirements:

- Ubuntu 16.04 LTS. 
- Installation of python 3. 
- Nvidia CUDA-capable GPU(GeForce GTX 1060 6GB and up).
- Installation of CUDA>=9.0, Nvidia-driver>=384.81.

## Installation

### Before Installing

- Verify your device meets minimum requirements above.
- Pickup a ledger from [orion ledger list](https://orioncloud.io/dashboard/#/worker/general).
- [Create an NBAI wallet](https://medium.com/nebula-ai/wallet-instruction-5748c950d556) for receiving rewards.

### Download and initialize 

1. Download latest released [AI worker package](https://github.com/nebulaai/ai-worker/releases), unzip file manually and extract with Archive Manager. 
2. Open your extracted folder, right-click and select "Open in Terminal", execute the following command:
  
 ```
$ chmod +x nbai.sh
$ ./nbai.sh
 ```
   
*Note*: You will be asked to type in administrator password at this step. Answer "Yes" or "Y" while being asked. 
                                                                                                               
### Pull NBAI docker image

Restart your system, in order to enable root permission for the following steps.

*Note*: Re-execute nbai.sh if permission denied from Docker Daemon.

Open your folder, right-click and select "Open in Terminal":

 ```
$ docker pull nbaicloudplatform/tf1.8_torch_cuda9:latest
 ```
 
### Join ledger group

1. Open your extracted folder, execute in terminal:

 ```
$ python3 manager.py
 ```
 
2. Enter ledger node url, NBAI wallet address and ledger url ([ledger list](https://orioncloud.io/dashboard/#/worker/general)).

A benchmark test will be executed on your machine. You will see your benchmark score in terminal prompt.

### Make Deposit

For first time worker joining, all workers are required to make a credit deposit to their selected ledger. 
Keep your terminal open and open the file _/worker deposit/index.html_ :

1. In your browser page, enter your ledger info and click" Load Ledger".
2. Enter your wallet and click "Load Wallet".
*Note*: This wallet is used for making deposit. You may use the same NBAI wallet for deposit and receiving rewards. 
3. Enter your worker ID, click “Load Worker”.
4. Enter the amount of NBAI you will deposit for this worker ID. Click "Deposit".
  
*Note*: If transaction is successful, a "Deposit successful" will be displayed on browser within seconds. Click again “Load Worker” you will now see "Eligible".

You are all set! The following message on your terminal showed that you have joined orion successfully. New tasks will be automatically sent to you.

```
 2019-01-21 22:12:10-INFO- Worker has joined queue
 2019-01-21 22:12:10-INFO- Worker has started heartbeat successfully
 2019-01-21 22:12:10-INFO- Worker is waiting for a task...
```

## Release History

2019-01-23

 **v1.1.1**
 - Automatically verify port listening status.
 - Add worker ID, task ID in script execution log.
 - Re-define hardware and installed software information for benchmarking
 - Add interruption handling in case of worker forced exit.

2018-12-11 

  **v0.1.1**
- Add task script running Traceback in execution log
- Fix issue on network connection between worker and ledger

2018-11-22

 **v0.0.1**                                          
- Add UTC timestamp in worker terminal prompt                
- Bug fix: Resolve and specify hardware recognition error 

2018-11-16

**pre-release**
- initial version
  

## Getting help

For questions, issues regarding ai worker, please submit [email requests](https://orioncloud.io/contact.html).

## Licence

All code is licenced under GNU General Public License v3.0.

## Resources

* [Orion cloud website](https://orioncloud.io/)
* [Orion cloud user guide](https://orioncloud.io/ai.html)
* [Orion cloud AI worker](https://orioncloud.io/ai-workers.html)
* [Nebula AI block browser](https://scan.nbai.io/#/)
* [Nebula AI Blockchain Node](https://github.com/nebulaai/nbai-node)
* [Nvidia-drivers](https://www.nvidia.com/Download/index.aspx)
