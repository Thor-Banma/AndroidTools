## 1. Android Studio 创建虚拟机的时候，提示HAXM未安装或者不是最新版本
Android Studio创建虚拟机的时候，提示HAXM未安装，根据内置的引导进行安装的时候，会报错，提示去看[Github](https://github.com/intel/haxm/wiki/Installation-Instructions-on-Windows)的教程。根据教程先去[Intel下载HAXM的Release版本](https://github.com/intel/haxm/releases),安装好之后，再次创建虚拟机，提示HAXM is out of date。此时需要修改两处地方：
- BIOS中打开Virtualization Technology以及VT-D的开关，使其Enabled
- 在control panel的programs and features中， 选择Turn Windows features on or off，然后勾选Virtual Machine Platform和Windows Hypervisor Platform
参考视频：[Fixed - Android Studio Reinstall HAXM | Virtual machine acceleration driver is out of date](https://www.youtube.com/watch?v=9l3TfjE-DaA)
参考文档：[我的处理器是否支持英特尔® 虚拟化技术？](https://www.intel.cn/content/www/cn/zh/support/articles/000005486/processors.html)
