# asus-FX504GE_FX80GE-efi-oc0.7.2
hackintosh 黑苹果

已正确驱动big sur 11.5，可进行系统更新

处理器 英特尔i5-8300h

在 yongjie520大佬的efi基础上进行升级，将opencore升级到0.7.2，kext驱动全部升级

缺陷：1.wifi、蓝牙无法驱动，解决办法只能更换博通网卡，建议更换bcm943224pcie
  2.3.5mm耳机孔播放出的声音有问题
     
 注意 usbinjectall.kext这个驱动被我替换成了usbports.kext，因为其在macos11.3x之后无法正确驱动，会导致usb插入接口后没反应，也就无法使用usb鼠标等。
 
 这点显示在黑果小兵的提示中，解决方法是需要定制usb的kext（bilibili很多教程），每个人的usb定制各不相同（不确定笔记本是否都一样）
 
 建议把我的usbports.kext删除后换上usbinjectall.kext，并用occ打开config.plist将usbinjectall.kext勾选上，刷入11.2系统再定制自己的usb，定制好后就可以ota升级了

