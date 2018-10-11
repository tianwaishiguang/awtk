# AWTK 调试技巧

这里收集一些调试技巧，各种疑难杂症的解决方案。请大家把遇到的问题(包括已经解决的)发到issues上，我来收集整理。谢谢


## 一、输入设备相关问题

## 二、显示相关问题

* 1.图片颜色不正常

## 三、资源相关问题

## 四、内存问题

* 1.内存出现莫名其妙的错误

> 通常是堆栈溢出，把栈空间修改大点试试。如果支持jpg/png，栈至少32K。

* 2.内存泄露

> 如果定义宏了ENABLE\_MEM\_LEAK\_CHECK，每次内存分配都会记录分配的位置、大小和时间，并在窗口打开和关闭时，通过log_debug显示当前未释放的内存块。根据块数的变化可以看出是否有内存泄露，并根据分配的位置可以定位泄露的位置。
> 