# Gigabyte-Z390-Gaming-X-Hackintosh
## 硬件配置
| 类型 | 型号 |
| :----:| :----:|
| 主板 | 技嘉z390 gaming x |
| CPU | i5 9600K |
| 显卡 | RX 590 |
| 内存 | 海盗船复仇者 2666 *2 |
| 无线网卡、蓝牙 | BCM94360CD |
| 固态 | 金士顿480G |
| 电源 | 振华 LG650W全模组 |  

## 长期更新
## 2020-6
最新版使用oc引导，知道如何将CFG关闭的，可以直接使用我的，不知道如何关闭的，修改AppleCpuPmCfgLock，AppleXcpmCfgLock，参考地方为: https://dortania.github.io/OpenCore-Desktop-Guide/config.plist/coffee-lake.html
## 2020-1-8更新
使用一段时间后重装为10.14.3版本（没办法，轻微强迫症，看到一些地方不正常就想改），目前基本已经全部完美,测试可以硬件加速（使用videoproc测试，和vdadecoderchecker测试），也能打开finalcutpro，没闪退。一切运行正常  
![https://github.com/wqh0109663/Gigabyte-Z390-Gaming-X-Hackintosh/blob/master/screen%20shot/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202020-01-07%20%E4%B8%8B%E5%8D%8810.31.45.png](https://github.com/wqh0109663/Gigabyte-Z390-Gaming-X-Hackintosh/blob/master/screen%20shot/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202020-01-07%20%E4%B8%8B%E5%8D%8810.31.45.png)
![https://github.com/wqh0109663/Gigabyte-Z390-Gaming-X-Hackintosh/blob/master/screen%20shot/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202020-01-07%20%E4%B8%8B%E5%8D%8811.40.59.png](https://github.com/wqh0109663/Gigabyte-Z390-Gaming-X-Hackintosh/blob/master/screen%20shot/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202020-01-07%20%E4%B8%8B%E5%8D%8811.40.59.png)
![https://github.com/wqh0109663/Gigabyte-Z390-Gaming-X-Hackintosh/blob/master/screen%20shot/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202020-01-08%20%E4%B8%8B%E5%8D%8810.35.42.png](https://github.com/wqh0109663/Gigabyte-Z390-Gaming-X-Hackintosh/blob/master/screen%20shot/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202020-01-08%20%E4%B8%8B%E5%8D%8810.35.42.png)
### 安装方法
1. 下载链接
https://mirrors.dtops.cc/iso/MacOS/daliansky_macos/10.14/macOS%20Mojave%2010.14.3%2818D42%29%20Installer%20with%20Clover%204859.dmg
1. bios设置
在bios按照 Windows 8/10 设置为other，csm support 设置为disable，secure boot设置为disabled，peripherals里面 initial display 设置为pcie 1 slot，power 里面erp设置为enabled，然后把internal graphics设置为enabled，然后就是超频的设置，看你个人喜好了，我是cpu设置的47，然后内存条是2666，打开xmp，然后核显使用128(dvmt pre allocated 128M)，截图的话，screenshot文件夹下有部分，唯一不同的只有我这个版本把核显预分配设置为了128M
2. 安装前的准备
下载10.14.3（我使用的是小兵的镜像文件），制作u盘启动盘（16G），于drivers64UEFI目录中移除AptioMemoryFix-64.efi添加OsxAptioFix2Drv-free2000.efi该驱动位于/EFI/CLOVER/drivers-off目录下，格式化固态硬盘
3. 安装
磁盘工具抹掉硬盘之后，直接选择终端，在终端中输入 date 0201010116,后面毫无阻碍
4. 或者就是直接使用另一个大白菜u盘直接替换掉u盘中的efi文件夹
5. 更换机型和序列号
6. 中途可能会遇到panic，重启就好，建议多存几分config，如果突然启动不了了，可以有其他config可以选择，或者是如果自己打补丁，进不了系统的，可以考虑使用u盘引导进入，实在不行，使用大白菜diskgenius直接修改efi文件夹中的内容
-----


声明：修改序列号，避免发生冲突
当前版本是10.15.2 (19C57)，历史版本自己下
## screen shot
BIOS设置自己去看screen shot文件夹
![https://github.com/wqh0109663/Gigabyte-Z390-Gaming-X-Hackintosh/blob/master/screen%20shot/Screen%20Shot%202019-11-28%20at%2021.14.55.png](https://github.com/wqh0109663/Gigabyte-Z390-Gaming-X-Hackintosh/blob/master/screen%20shot/Screen%20Shot%202019-11-28%20at%2021.14.55.png)
![https://github.com/wqh0109663/Gigabyte-Z390-Gaming-X-Hackintosh/blob/master/screen%20shot/Screen%20Shot%202019-11-28%20at%2021.15.26.png](https://github.com/wqh0109663/Gigabyte-Z390-Gaming-X-Hackintosh/blob/master/screen%20shot/Screen%20Shot%202019-11-28%20at%2021.15.26.png)
![https://github.com/wqh0109663/Gigabyte-Z390-Gaming-X-Hackintosh/blob/master/screen%20shot/Screen%20Shot%202019-11-28%20at%2021.15.44.png](https://github.com/wqh0109663/Gigabyte-Z390-Gaming-X-Hackintosh/blob/master/screen%20shot/Screen%20Shot%202019-11-28%20at%2021.15.44.png)
![https://github.com/wqh0109663/Gigabyte-Z390-Gaming-X-Hackintosh/blob/master/screen%20shot/Screen%20Shot%202019-11-28%20at%2021.17.10.png](https://github.com/wqh0109663/Gigabyte-Z390-Gaming-X-Hackintosh/blob/master/screen%20shot/Screen%20Shot%202019-11-28%20at%2021.17.10.png)
