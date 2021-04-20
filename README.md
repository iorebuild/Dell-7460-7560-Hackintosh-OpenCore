# Dell-7460/7560-Hackintosh-OpenCore

## 电脑配置

核心显卡：hd620（已完美驱动）

独立显卡：NVIDIA 940mx（不可能驱动），so nvidia fuck you！

CPU：i5 7200u（我依然觉得CPU会热，希望大佬解决）

网卡：intel3165（自带无线网卡已经放置驱动，原生即可使用）

声卡：alc256（安装耳麦补丁基本完美）

蓝牙：已经驱动但是不完美，断断续续，可能和无线驱动有关

### 需要的配置

#### 	解锁cfg_lock，如果未解锁请bilibili搜索cfglock参考我的视频解锁

（这是个技术活，失败弄坏电脑本人不承担责任）

#### 清除NVRAM

​	安装好系统后请在OpenCore的引导页面按下空格选择restart nvram然后在bios中重新添加引导

#### 耳麦配置

耳麦插件的kext已经放到放进去了只需要安装补丁即可

https://github.com/hackintosh-stuff/ComboJack

#### 发热解决

​	发热原因为睿频导致，关闭睿频即可（工具如下）

http://tbswitcher.rugarciap.com

​	下载free免费版本即可

#### 关闭休眠

实测容易睡死，建议关闭睡眠

```
sudo pmset -b sleep 0; sudo pmset -b disablesleep 1
```

#### 开机HI-DPI

https://github.com/xzhih/one-key-hidpi

#### 其他注意事项

！！！如果安装的是Catalina请不要更新系统，就算是个小补丁也不要更新，会导致Window Server和Kernel_task占用大量的CPU，BigSur没测试，因为很卡不想用