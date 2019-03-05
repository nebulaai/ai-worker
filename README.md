
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

# Nebula AI Worker v2

This instruction is for Nebula AI Worker v2.

### Prerequisites

##### Hardware

* CPU

    Intel Sandy Bridge (2011) or later, Core i3 or higher class
    
* GPU

    One or more NVIDIA® GPU card with CUDA® Compute Capability 3.5 or higher. See the list of [CUDA-enabled GPU cards](https://developer.nvidia.com/cuda-gpus).

##### System

* Ubuntu 18.04 LTS is preferred
* Ubuntu 16.04 LTS is Compatible
* A new installed system is preferred
 
##### Other
* A NBAI wallet having NBAI (having both wallet address and private key)

### Installation

**Warning: Please backup all personal data before any following step.**

 * Extract 'nbai_worker' folder out of the zip file.
 * Open a terminal on the folder just extracted(right click on the folder and select 'Open in Terminal'), and enter
 
 ```bash
 cd ./installer
 chmod +x ./install.sh
 sudo ./install.sh
 ```   
 
 * Follow the information prompt
 * Reboot is required
 
### Configuration
    
##### Example

   ```json
      {
         "ledger": "http://54.211.127.67:8080",
         "node": "http://18.215.32.172:8051",
         "wallet": "0xeF980D9ACB9Bd396b38b0A0A5de834d70A9b9125",
         "price_limit": "1",
         "dual_mode": true
      }
   ```
   1. "ledger" and "node" are on your choice. You can choose you preferred service provider or use the default we provided.
      
      Check our [Orion cloud](https://orioncloud.io/dashboard/#/worker/general) for all available official choices.
      
   2. "wallet" is used to pay and receive NBAI. Deposit for worker will be charged to this wallet, and output from mining and doing task will be saved to this wallet.
      
      Please make sure you have the **private key** of this wallet for future usage.
      
   3. "price_limit" is recommended to keep as default.
   
   4. "dual_mode" controls 'mining when idle' functionality.
   
      * When true, worker will mine NBAI when waiting for a task.
      * When false, worker will not mine NBAI when waiting for a task.
 
### Launching
                  
 * In the terminal, enter
 ```bash
 ./launch_nbai_worker
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
