### EFI概述

> 通过 [Dortania](https://dortania.github.io/OpenCore-Desktop-Guide/AMD/zen.html) 和 [XJN](https://blog.xjn819.com/?p=543) 的博客，定制OpenCore引导

Mac 版本：10.15.4

Opencore 版本：0.5.8

更新日期：2020-05-05



### 配置清单

| 类型 | 型号              |
| ---- | ----------------- |
| 主板 | 微星 B450m 迫击炮 |
| CPU  | AMD R5 3600x      |
| 显卡 | 蓝宝石 RX 570     |



### 功能测试

##### 正常使用功能

* 前后端声音输出
* USB
* 有线网络
* iMessage、FaceTime
* 独显硬件加速
* 睡眠唤醒（需将键鼠接到USB2.0端口，按开机键唤醒）

##### 不能使用

* 内置麦克风



### 注意事项

1. 如遇到黑屏情况，请尝试加启动参数`agdpmod=pikera`
2. 声卡不能正常工作，请尝试更换启动参数中`alcid=1`的值
3. 睡眠后RTC自动唤醒，请打开`Kernel->Patch->Disable RTC wake scheduling`



### 你可能需要做的事

1. 使用Hackintool等工具重新生成三码
2. 参考 [Dortania](https://dortania.github.io/OpenCore-Desktop-Guide/AMD/zen.html) 和 [XJN](https://blog.xjn819.com/?p=543) 的博客，对一些自定义的选项进行修改



### 致谢

* [黑果小兵的部落阁](https://blog.daliansky.net)
* [XJN'S BLOG](https://blog.xjn819.com)
* [Dortania](https://dortania.github.io/OpenCore-Desktop-Guide/AMD/zen.html)