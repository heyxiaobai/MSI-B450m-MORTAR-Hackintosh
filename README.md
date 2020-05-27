### EFI概述

> 通过 [Dortania](https://dortania.github.io/OpenCore-Desktop-Guide/AMD/zen.html) 和 [XJN](https://blog.xjn819.com/?p=543) 的博客，定制OpenCore引导

Mac 版本：10.15.5

Opencore 版本：0.5.8

更新日期：2020-05-27



### 配置清单

| 类型 | 型号              |
| ---- | ----------------- |
| 主板 | 微星 B450m 迫击炮 |
| CPU  | AMD R5 3600x      |
| 显卡 | 蓝宝石 RX 570     |



### 功能测试

##### 正常使用功能

* 前后端声音输出
* 所有USB端口
* 有线网络
* iMessage、FaceTime
* 独显硬件加速
* 睡眠唤醒（需将键鼠接到USB2.0端口，按开机键唤醒）

##### 不能使用

* 内置麦克风（使用USB/蓝牙音箱的麦克风或者使用`VoodooHDA`解决)



### BIOS推荐设置

#### 禁用

* Fast Boot -- 快速启动
* CSM -- 兼容性支持模块

#### 启用

* Above 4G decoding -- 4G以上解码（**启用此项后需移除启动参数中的`npci=0x2000`**）
* EHCI/XHCI Hand-off
* OS type: Windows 8.1/10 UEFI Mode -- 操作系统类型



### 注意事项

1. 如遇到黑屏情况，请尝试加启动参数`agdpmod=pikera`
2. 默认注入声卡`ID`为`1`，如不能正常工作请尝试更换启动参数中`alcid=1`的值
3. 默认使用`RealtekRTL8111.kext`，其他有线网卡自行更换驱动
4. 避免与他人重复序列号，请使用`Hackintool`等工具重新生成三码
5. 睡眠后RTC自动唤醒，请打开`Kernel->Patch->Disable RTC wake scheduling`
6. 建议参考 [Dortania](https://dortania.github.io/OpenCore-Desktop-Guide/AMD/zen.html) 和 [XJN](https://blog.xjn819.com/?p=543) 的博客，对一些自定义的选项进行修改



### 致谢

* [黑果小兵的部落阁](https://blog.daliansky.net)
* [XJN'S BLOG](https://blog.xjn819.com)
* [Dortania](https://dortania.github.io/OpenCore-Desktop-Guide/AMD/zen.html)