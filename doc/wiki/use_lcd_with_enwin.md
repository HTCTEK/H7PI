#### LCD接口
LCD接口参数请参考：[LCD接口](https://gitee.com/Pinno/H7PI/wikis/LCD%E6%8E%A5%E5%8F%A3?sort_id=1717179)

#### STemWin
* H7PI和H7PI_Samples默认已经支持STemWin，并且适配了2.8寸的240x320显示屏（下方的要点可以忽略）
* 使用STemWin需要打开STM32的硬件CRC功能，默认已经打开
* 在GUIConf.c中可以定义GUI的缓存，在GUIConf.h中额可以定义GUI的一些配置功能，例如使用os
* 在LCDConf_FlexColor_Template.c文件中，把LCD驱动函数（..\User\Drivers\LCDConf.c）填充进STemWin的API函数


#### 使用H7PI_Samples
* 下载H7PI_Sample工程 [H7PI_Sample](https://gitee.com/Pinno/H7PI_Samples)

* 下载H7PI_MultiBootloader工程 [H7PI_MultiBootloader](https://gitee.com/Pinno/H7PI_MultiBootloader)

* 查看SWD接口说明 [SWD接口](https://gitee.com/Pinno/H7PI/wikis/SWD%E6%8E%A5%E5%8F%A3?sort_id=1735245) 并接线，连接USB供电

* 下载bootloader，为app做准备 
![下载bootloader](https://images.gitee.com/uploads/images/2019/1128/095128_7972faed_1586921.jpeg "下载MultiBootloader.jpg")

* 打开H7PI_Samples，下载app_test程序，LED1为绿灯，LED2为红灯，同时每1S会刷新LCD屏幕上的数字，屏幕上的数字就是系统嘀嗒时钟。
![下载测试程序](https://images.gitee.com/uploads/images/2019/1128/095937_6a4f30d6_1586921.jpeg "123.jpg")