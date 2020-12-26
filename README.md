### EFI概述

> 通过 [Dortania](https://dortania.github.io/OpenCore-Desktop-Guide/AMD/zen.html) 定制OpenCore引导，**请自行参考进行一些自定义的修改**
>
> 因主用Intel平台，此EFI可能会更新不及时，且新版本未进行长时间的测试，有问题可以随时反馈，请多见谅！

Mac 版本：11.1

Opencore 版本：0.6.4

更新日期：2020-12-26





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
* 睡眠/唤醒（键鼠不能接到后面的`USB3.0`端口）

##### 不能使用

* 内置麦克风（使用USB/蓝牙音箱的麦克风或者使用`VoodooHDA`解决)



### BIOS推荐设置

* 高级 -- windows操作系统的配置 -- `CSM` 改为 `UEFI`
* 高级 -- windows操作系统的配置 -- 安全引导 -- 禁止安全启动（默认禁止）
* 高级 -- USB设置 -- XHCI Hand-off -- 开启（默认开启）



### 注意事项

1. **登陆Apple ID前请先使用`Hackintool`等工具重新生成序列号等信息，避免与他人重复**
2. 如遇到黑屏情况，尝试增加启动参数`agdpmod=pikera`
3. 需要在引导界面开启HiDPI模式，请将`NVRAM -> Add -> 4D1EDE05-38C7-4A6A-9CC6-4BCCA8B38C14 -> UIScale`设置为`02`
4. 默认注入声卡`ID`为`1`，如不能正常工作请尝试更换启动参数中`alcid=1`的值
5. 默认使用`RealtekRTL8111.kext`并内建，其他主板/有线网卡请自行更换
6. 如遇 TV、Netflix 等带有 DRM 的视频解码黑屏问题，请尝试在启动参数中添加`shikigva=80`【感谢[@Butanediol](https://github.com/Butanediol)】



### 致谢

* [Dortania](https://dortania.github.io/OpenCore-Install-Guide/AMD/zen.html)
* [黑果小兵的部落阁](https://blog.daliansky.net)
* [XJN'S BLOG](https://blog.xjn819.com)
