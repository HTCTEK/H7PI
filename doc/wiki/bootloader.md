#### 为什么需要Bootloader
如果程序不大，出厂不需要OTA，可以不使用Bootloader，H7PI自带了TFT接口，为了应对更大的程序要求和储存空间要求，使用了QSPI flash作为程序空间，因此，需要一个bootloader在上电后映射flash的地址空间和跳转。

#### H7PI的bootloader
H7PI的bootloader目前支持文件系统，通过IO1和3V3的短接，插入USB上电后，可以枚举出一个U盘，把bin文件和一个json配置文件放入update文件夹，并放置到U盘根目录，断开USB和IO1的短接，重新上电即可自动更新。

当然，如果有读卡器，可以按照同样的方法把文件存入TF卡（MicroSD），插入H7PI后直接上点即可更新，注意path中路径需要使用0:/磁盘号

#### 如何进入U盘更新模式
1. 短接3V3和IO1(PD10)
2. 通过USB接口接入电脑，此时电脑枚举出8MB的U盘
3. 新建一个update文件夹，将固件放入update文件夹
4. 在update文件夹新建一个json文件，命名为fw.json
5. 在fw.json文件中建立三个字段如下：

```
{
    "path":"1:/update/app_test.bin",
    "version":"0.1",
    "crc32":"653E571F"
}
```
6. path字段为固件路径，spiflash请使用磁盘号1，SD Card请使用磁盘号0
7. crc32 请使用hash工具计算bin文件的crc32值，并填入字段
8. 目前没有对版本号进行比较，version无关紧要