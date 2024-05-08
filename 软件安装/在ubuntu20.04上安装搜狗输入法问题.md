- [1. 官方安装步骤](#1-官方安装步骤)
- [2. 问题](#2-问题)
- [3. 问题查找与解决](#3-问题查找与解决)

### 1. 官方安装步骤
[ubuntu 安装搜狗输入法步骤](https://shurufa.sogou.com/linux/guide)

### 2. 问题
1. 输入法可以切换，但是无法输入中文
2. 搜狗的输入法图标无法打开设置
3. 使用命令行重启`fcitx`报错：
```
...

(ERROR-5248 module.c:66) fcitx-sogoupinyinhxm ABI Version Error
(ERROR-5248 ime.c:432) fcitx-keyboard-in-tel-kagapa already exists
(ERROR-5248 ime.c:432) fcitx-keyboard-cm-mmuock already exists
parse /home/zhangym/.config/sogoupinyin//logf.conf fail
auth ok
/opt/sogoupinyin/files/bin/sogoupinyin-watchdog: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Gui.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-watchdog)
/opt/sogoupinyin/files/bin/sogoupinyin-watchdog: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Widgets.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-watchdog)
/opt/sogoupinyin/files/bin/sogoupinyin-watchdog: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Core.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-watchdog)
/opt/sogoupinyin/files/bin/sogoupinyin-watchdog: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Core.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-watchdog)
/opt/sogoupinyin/files/bin/sogoupinyin-watchdog: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5DBus.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-watchdog)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Qml.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-service)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5DBus.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-service)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Gui.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-service)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Widgets.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-service)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Core.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-service)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Core.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-service)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Widgets.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouIme.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Gui.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouIme.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Core.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouIme.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Core.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouIme.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5DBus.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouIme.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5DBus.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouShell.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Gui.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouShell.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Core.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouShell.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Core.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouShell.so)
/opt/sogoupinyin/files/bin/sogoupinyin-watchdog: symbol lookup error: /opt/sogoupinyin/files/bin/sogoupinyin-watchdog: undefined symbol: qt_version_tag, version Qt_5.6
err: can't open sendmq:-1, mq:5248, /SOGOUPINYIN-SOGOU-IME-IPC-MQ-9999-9999-1000-0
/opt/sogoupinyin/files/bin/sogoupinyin-service: symbol lookup error: /opt/sogoupinyin/files/bin/../lib/libSogouShell.so: undefined symbol: qt_version_tag, version Qt_5.6
err: can't open sendmq:-1, mq:5248, /SOGOUPINYIN-SOGOU-IME-IPC-MQ-9999-9999-1000-0
err: can't open sendmq:-1, mq:5248, /SOGOUPINYIN-SOGOU-IME-IPC-MQ-9999-9999-1000-0
err: can't open sendmq:-1, mq:5248, /SOGOUPINYIN-SOGOU-IME-IPC-MQ-9999-9999-1000-0
err: can't open sendmq:-1, mq:5248, /SOGOUPINYIN-SOGOU-IME-IPC-MQ-9999-9999-1000-0
err: can't open sendmq:-1, mq:5248, /SOGOUPINYIN-SOGOU-IME-IPC-MQ-9999-9999-1000-0
err: can't open sendmq:-1, mq:5248, /SOGOUPINYIN-SOGOU-IME-IPC-MQ-9999-9999-1000-0
err: can't open sendmq:-1, mq:5248, /SOGOUPINYIN-SOGOU-IME-IPC-MQ-9999-9999-1000-0

...
```

### 3. 问题查找与解决
1. 查看其动态链接库：`ldd /opt/sogoupinyin/files/bin/sogoupinyin-service`
```
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Qml.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-service)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5DBus.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-service)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Gui.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-service)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Widgets.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-service)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Core.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-service)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Core.so.5: no version information available (required by /opt/sogoupinyin/files/bin/sogoupinyin-service)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Widgets.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouIme.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Gui.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouIme.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Core.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouIme.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Core.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouIme.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5DBus.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouIme.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5DBus.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouShell.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Gui.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouShell.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Core.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouShell.so)
/opt/sogoupinyin/files/bin/sogoupinyin-service: /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5Core.so.5: no version information available (required by /opt/sogoupinyin/files/bin/../lib/libSogouShell.so)
	linux-vdso.so.1 (0x00007ffc8e7ad000)
	libQt5DBus.so.5 => /opt/sogoupinyin/files/bin/../lib/qt5/lib/libQt5DBus.so.5 (0x00007f334be00000)

...
```
显示确实有依赖的动态库没有版本信息。    
2. 使用系统自带的`Qt`库进行替换 
`sudo cp -ar /usr/lib/x86_64-linux-gnu/libQt* /opt/sogoupinyin/files/bin/../lib/qt5/lib/`   
重启`fcitx`显示正常
