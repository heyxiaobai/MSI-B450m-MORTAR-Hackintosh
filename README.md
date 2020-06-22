### EFI概述

> 通过 [Dortania](https://dortania.github.io/OpenCore-Desktop-Guide/AMD/zen.html) 和 [XJN](https://blog.xjn819.com/?p=543) 的博客，定制OpenCore引导，**建议参考博客内容做一些自定义的修改**

Mac 版本：10.15.5

Opencore 版本：0.5.9

更新日期：2020-06-22



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
* 手动睡眠/唤醒（键鼠不能接到后面的`USB3.0`端口）

##### 不能使用

* 内置麦克风（使用USB/蓝牙音箱的麦克风或者使用`VoodooHDA`解决)
* 自动睡眠（疑似`XHC0`的问题）



### BIOS推荐设置

* 高级 -- windows操作系统的配置 -- `CSM` 改为 `UEFI`
* 高级 -- windows操作系统的配置 -- 安全引导 -- 禁止安全启动（默认禁止）
* 高级 -- USB设置 -- XHCI Hand-off -- 开启（默认开启）



### 注意事项

1. **登陆Apple ID前请先使用`Hackintool`等工具重新生成序列号等信息，避免与他人重复**
2. 如遇到黑屏情况，请尝试加启动参数`agdpmod=pikera`
3. 默认注入声卡`ID`为`1`，如不能正常工作请尝试更换启动参数中`alcid=1`的值
4. 默认使用`RealtekRTL8111.kext`，其他有线网卡自行更换



### 致谢

* [黑果小兵的部落阁](https://blog.daliansky.net)
* [XJN'S BLOG](https://blog.xjn819.com)
* [Dortania](https://dortania.github.io/OpenCore-Desktop-Guide/AMD/zen.html)