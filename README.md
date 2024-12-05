# 华为手机通过ADB永久关闭系统更新

本文详细介绍了如何在华为手机上禁用系统更新的弹窗提示，包括去除系统更新小红点、开启调试模式以及使用ADB工具进行系统更新的关闭和恢复。此方法适用于不想频繁收到系统更新提示的用户。

## 操作步骤

### 一、去除系统更新的小红点
1. 关闭手机的WIFI和数据网络（4G）。
2. 进入“设置” --> “应用和通知” --> “应用管理”，找到“系统更新”，点开“存储”，执行删除数据和清空缓存操作。

### 二、打开调试模式
1. 进入“设置” --> “系统” --> “关于手机”，连续点击7次“版本号”栏，屏幕将出现提示“您正处于开发者模式”。
2. 返回上一步“系统”界面，打开“开发人员选项”，关闭“自动系统更新”，打开“USB调试”以及打开“仅充电”模式下允许ADB调试。

### 三、ADB操作
1. 下载ADB和驱动，安装驱动。
2. 解压下载包中的adb到C盘。
3. 在C盘adb文件夹上，按住Shift，点击鼠标右键，选择“在此处打开命令窗口（W）”，或者可以通过命令来打开，运行CMD，输入cd c:\adb。
4. 停止系统更新，CMD命令窗口输入命令：`adb shell pm disable-user com.huawei.android.hwouc`。
5. 等待adb成功关闭系统更新，重启手机即可。之后点击手机中的系统更新是点不开的。

### 恢复系统更新
如果要恢复开启系统更新，CMD命令窗口输入命令：`adb shell pm enable com.huawei.android.hwouc`。

通过以上步骤，您可以永久关闭华为手机的系统更新提示，避免频繁的更新弹窗干扰。

## 下载链接

[华为手机通过ADB永久关闭系统更新](https://pan.quark.cn/s/7beee30ab6c7)