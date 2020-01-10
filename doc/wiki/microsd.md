#### Micro SD 
Micro SD相当于平常我们所说的TF卡，较小的体积，可以实现较大得容量存储空间
![Micro SD卡接口](https://images.gitee.com/uploads/images/2019/1108/100822_24cf731e_1586921.png "TIM截图20191108100505.png")
![TF Card](https://images.gitee.com/uploads/images/2019/1108/100625_9bf4190c_1586921.png "TIM截图20191108100612.png")
#### 接口
1. Micro SD（TF Card）接口使用STM32 SDMMC2接口，支持DMA传输
2. 通过cubeMX可以调整接口频率，适应不同速度得卡，也可以通过低速读取卡的最大速度，再次调整频率以达到高速
3. 支持连接FatFS文件系统（其他也可以支持，主要实现文件系统API即可）