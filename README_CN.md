
**[什么是 AI Worker](#what-is-ai-worker)** | 
**[配置信息](#prerequisites)** |
**[安装](#installation)** |
**[历史版本](#release-history)** |
**[帮助](#getting-help)** | 
**[许可证](#licence)** |
**[相关资源](#resources)** |  

# [Nebula AI Worker](https://github.com/nebulaai/ai-worker)

Orion AI Worker 官方软件发布.

## AI Worker 版本 V2

**AI Workers** 是 [Orion 云计算平台](https://nbai.io/)中的资源提供者。他们执行 AI 任务并获得 NBAI 币作为奖励。
每个 GPU 机器可以下载最新的任务包，安装并加入 Orion 网络。 
通过简单地运行一些命令，Orion 的 AI 任务将自动被分配给 AI Worker，您将能够出租您的计算力以获得真正的利润。

### 配置信息

##### 硬件要求

* CPU

    Intel Sandy Bridge (2011) 架构或更新版本, 英特尔® 酷睿™ i3 处理器或更高。
    
* GPU

    至少一个具有 CUDA® Compute Capability 3.5 或更高算力的 NVIDIA® GPU 卡。查看 [具有 CUDA 的 NVIDIA® GPU 卡](https://developer.nvidia.com/cuda-gpus)。

##### 系统要求

* 推荐：Ubuntu 18.04 LTS
* 最低要求：Ubuntu 16.04 LTS
* 建议全新安装的系统
 
##### 其他
* 一个有 NBAI 币的 NBAI 钱包 (有钱包地址和私钥)

### 安装

**注意: 在继续以下步骤前，请备份您的个人资料。**

 * 从 zip 压缩文件中解压 'nbai_worker'。
 * 在刚解压缩的文件夹上打开终端 (鼠标右键点击文件夹选择 '在终端中打开'), 然后执行以下代码
 
 ```bash
 cd installer
 chmod +x ./install.sh
 sudo ./install.sh
 ```   
 
 * 按照信息提示操作
 * 需要重新启动电脑
 
### 配置
    
##### 例子

   ```json
      {
         "ledger": "http://54.211.127.67:8080",
         "node": "http://18.215.32.172:8051",
         "wallet": "0xeF980D9ACB9Bd396b38b0A0A5de834d70A9b9125",
         "price_limit": "1",
         "dual_mode": true
      }
   ```
   1. 您可以选择 "ledger" 和 "node"。您可以选择首选服务提供商或使用我们提供的默认服务。
      
      点击查看 [Orion cloud](https://nbai.io/dashboard/#/worker/general) 我们官方提供的服务选项。
      
   2. "wallet" 是用于支付和收取 NBAI 币。支付 Worker 的费用将会从此钱包中支出，挖矿和执行任务的收益将会存入此钱包。
      
      请确保您拥有此钱包的 **私钥** 以备将来使用。
      
   3. "price_limit" 建议保持默认状态。
   
   4. "dual_mode" 控制 '空闲时挖矿' 功能.
   
      * 设置为 true 时, Worker 将在等待任务时挖掘 NBAI。
      * 设置为 false 时, Worker 在等待任务时不会挖掘 NBAI。
 
### 发布
                  
 * 在终端输入
 ```bash
 ./launch_nbai_worker
 ```

## 历史版本

2019-03-05

 **v2.0.1**
 - 双挖掘模式
 - 在终端支付
 - 增加对 ubuntu 18.04 的支持
 
2019-01-23

 **v1.1.1**
 - 自动验证端口侦听状态。
 - 在脚本执行日志中添加 Worker ID，Task ID。
 - 重新定义硬件和已安装的软件信息以进行基准测试。
 - 在 Worker 强制退出的情况下添加中断处理。

2018-12-11 

  **v0.1.1**
- 在执行日志中添加运行Traceback的任务脚本
- 修复 worker 和 ledger 之间的网络连接问题

2018-11-22

 **v0.0.1**                                          
- 在工作终端提示符中添加UTC时间戳                
- 错误修复：解决并指定硬件识别错误

2018-11-16

**预览版**
- 初始版本
  

## 获得帮助

有关 AI Worker 的任何问题，请在此提交 [email requests](https://nbai.io/contact.html).

## 许可证

代码均已获得 GNU General Public License v3.0 的许可.

## Resources

* [Orion cloud 官网](https://nbai.io/)
* [Orion cloud 用户手册](https://nbai.io/ai.html)
* [Orion cloud AI worker](https://nbai.io/ai-workers.html)
* [Nebula AI block browser](https://scan.nbai.io/#/)
* [Nebula AI Blockchain Node](https://github.com/nebulaai/nbai-node)
* [Nvidia-drivers](https://www.nvidia.com/Download/index.aspx)
