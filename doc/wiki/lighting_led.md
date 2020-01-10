#### 板载LED使用的IO口
|  引脚   |  LED   |
| --- | --- |
|  PC14   |  LED-GREEN  |
|  PC15   |  LED-RED    |

![LED指示](https://images.gitee.com/uploads/images/2019/1128/094328_4dfe2ba7_1586921.jpeg "LED指示灯.jpg")

#### 使用H7PI_Sample工程  
* 下载H7PI_Sample工程 [H7PI_Sample](https://gitee.com/Pinno/H7PI_Samples)

* 下载H7PI_MultiBootloader工程 [H7PI_MultiBootloader](https://gitee.com/Pinno/H7PI_MultiBootloader)

* 查看SWD接口说明 [SWD接口](https://gitee.com/Pinno/H7PI/wikis/SWD%E6%8E%A5%E5%8F%A3?sort_id=1735245) 并接线，连接USB供电

* 下载bootloader，为app做准备 
![下载bootloader](https://images.gitee.com/uploads/images/2019/1128/095128_7972faed_1586921.jpeg "下载MultiBootloader.jpg")

* 打开H7PI_Samples，下载app_test程序，LED1为绿灯，LED2为红灯，在app_test_task中可以改变LED闪烁的效果
![下载测试程序](https://images.gitee.com/uploads/images/2019/1128/095937_6a4f30d6_1586921.jpeg "123.jpg")
