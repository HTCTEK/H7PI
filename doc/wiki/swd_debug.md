#### 串行调试（Serial Wire Debug）
SWD只需要4个（或者5个）引脚，结构简单，但是使用范围没有JTAG广泛，主流调试器上也是后来才加的SWD调试模式。

#### H7PI的SWD接口
H7PI的SWD接口使用3线或4线，主要看调试器是否需要VCC检测引脚或者能否给H7PI供电,VCC可以不接

| 信号 | 引脚 | 
|---|---|
| VCC检测     | 3V3       |
| GND        | GND       |
| TMS(SWDIO) | IO4(PA13) |
| TCK(SWDCLK)| IO5(PA14) |


