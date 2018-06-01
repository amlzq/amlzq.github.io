---
layout: post
title:  "GooglePixel设备"
date:   2018-06-01 00:00 +0800
categories: jekyll update
---
### ### device info
* IMEI/MEID
> 

### Factory Images

* 刷机步骤
```
target didn't report max-download-size
sending 'bootloader' (32248 KB)...
FAILED (command write failed (No error))
finished. total time: 0.011s
rebooting into bootloader...
FAILED (command write failed (No error))
finished. total time: 0.005s
target didn't report max-download-size
sending 'radio' (57320 KB)...
FAILED (command write failed (No error))
finished. total time: 0.011s
rebooting into bootloader...
FAILED (command write failed (No error))
finished. total time: 0.014s
extracting android-info.txt (0 MB) to RAM...
extracting boot.img (28 MB) to disk... took 0.196s
target didn't report max-download-size
archive does not contain 'boot.sig'
archive does not contain 'dtbo.img'
archive does not contain 'dt.img'
archive does not contain 'recovery.img'
extracting system.img (1752 MB) to disk... took 11.952s
archive does not contain 'system.sig'
archive does not contain 'vbmeta.img'
extracting vendor.img (251 MB) to disk... took 8.605s
archive does not contain 'vendor.sig'
wiping userdata...
Erase successful, but not automatically formatting.
Can't determine partition type.
FAILED (command write failed (No error))
--------------------------------------------
getvar:version-bootloader FAILED (command write failed (No error))
finished. total time: 0.004s
Press any key to exit...
```

* 解决方法
[archive does not contain "boot.sig"](http://tieba.baidu.com/p/3812140218)
```
image-hammerhead-lmy48b.zip里面的也解压出来。还要修改flash-all.bat
否则可能会出现，
1，写入system.img失败之类的（提示找不到或者内存不足之类的）
2，把32G刷成16G（5.x之后的官方刷机包都有这个问题）
flash-all.bat里的
fastboot -w update image-hammerhead-lmy48b.zip
修改为：
fastboot flash recovery recovery.img
fastboot flash boot boot.img
fastboot flash system system.img
::下面是清除个人数据的（双WIPE）。 如果要保留数据升级，则不要下面2行。
fastboot flash cache cache.img
fastboot flash userdata userdata.img
```

* 通过清理C盘至少有6G空间，内存至少有60%空闲，刷机成功
```
D:\GoogleChromeDownloads\ThirdParty_Android\googleRom\sailfish-opm2.171019.029>flash-all.bat
target reported max download size of 536870912 bytes
sending 'bootloader_b' (32248 KB)...
OKAY [  0.780s]
writing 'bootloader_b'...
(bootloader) Valid bootloader version.
(bootloader) Flashing active slot "_b"
(bootloader) Flashing active slot "_b"
OKAY [  9.844s]
finished. total time: 10.655s
rebooting into bootloader...
OKAY [  0.047s]
finished. total time: 0.047s
< waiting for any device >
target reported max download size of 536870912 bytes
sending 'radio_b' (57320 KB)...
OKAY [  1.824s]
writing 'radio_b'...
OKAY [  0.842s]
finished. total time: 2.682s
rebooting into bootloader...
OKAY [  0.047s]
finished. total time: 0.062s
extracting android-info.txt (0 MB) to RAM...
extracting boot.img (28 MB) to disk... took 0.210s
target reported max download size of 536870912 bytes
archive does not contain 'boot.sig'
archive does not contain 'boot_other.img'
archive does not contain 'dtbo.img'
archive does not contain 'dt.img'
archive does not contain 'recovery.img'
extracting system.img (1752 MB) to disk... took 80.865s
archive does not contain 'system.sig'
extracting system_other.img (551 MB) to disk... took 32.828s
archive does not contain 'system.sig'
archive does not contain 'vbmeta.img'
extracting vendor.img (251 MB) to disk... took 3.048s
archive does not contain 'vendor.sig'
archive does not contain 'vendor_other.img'
wiping userdata...
mke2fs 1.43.3 (04-Sep-2016)
Creating filesystem with 6509568 4k blocks and 1630208 inodes
Filesystem UUID: 1c51bcba-4762-11e8-aac5-c52a5511bec9
Superblock backups stored on blocks:
        32768, 98304, 163840, 229376, 294912, 819200, 884736, 1605632, 2654208,
        4096000

Allocating group tables: done
Writing inode tables: done
Creating journal (32768 blocks): done
Writing superblocks and filesystem accounting information: done

--------------------------------------------
Bootloader Version...: 8996-012001-1711291800
Baseband Version.....: 8996-130091-1802061512
Serial Number........: FA74T0302622
--------------------------------------------
checking product...
OKAY [  0.049s]
checking version-bootloader...
OKAY [  0.049s]
checking version-baseband...
OKAY [  0.062s]
sending 'boot_b' (28941 KB)...
OKAY [  0.701s]
writing 'boot_b'...
OKAY [  0.603s]
erasing 'system_b'...
OKAY [  1.043s]
sending sparse 'system_b' 1/4 (524284 KB)...
OKAY [ 12.272s]
writing 'system_b' 1/4...
OKAY [  4.187s]
sending sparse 'system_b' 2/4 (524284 KB)...
OKAY [ 12.365s]
writing 'system_b' 2/4...
OKAY [  4.125s]
sending sparse 'system_b' 3/4 (524284 KB)...
OKAY [ 12.063s]
writing 'system_b' 3/4...
OKAY [  4.128s]
sending sparse 'system_b' 4/4 (221352 KB)...
OKAY [  5.137s]
writing 'system_b' 4/4...
OKAY [  1.989s]
erasing 'system_a'...
OKAY [  1.105s]
sending sparse 'system_a' 1/2 (524284 KB)...
OKAY [ 12.168s]
writing 'system_a' 1/2...
OKAY [  4.193s]
sending sparse 'system_a' 2/2 (40684 KB)...
OKAY [  0.995s]
writing 'system_a' 2/2...
OKAY [  0.698s]
erasing 'vendor_b'...
OKAY [  0.497s]
sending 'vendor_b' (257044 KB)...
OKAY [  5.957s]
writing 'vendor_b'...
OKAY [  2.239s]
Setting current slot to 'b'...
OKAY [  0.396s]
erasing 'userdata'...
OKAY [  5.547s]
sending 'userdata' (4412 KB)...
OKAY [  0.155s]
writing 'userdata'...
OKAY [  0.196s]
rebooting...

finished. total time: 93.249s
Press any key to exit...
```


### Full OTA Images
```
C:\Users\asus>adb devices
List of devices attached
FA74T0302622    sideload
```

* 
```
C:\Users\asus>adb sideload D:\GoogleChromeDownloads\ThirdParty_Android\googleRom\sailfish-ota-opm2.171019.029-d0f1d78c.zip
serving: 'D:\GoogleChromeDownloads\ThirdParty_Android\googleRom\sailfish-ota-opm2.171019.029-d0f1d78c.zip'  (~30%)    adb: fa
iled to read command: Connection reset by peer
```

---
### 参考文章
* [文字说明][文字说明]
---
[文字说明]: 链接