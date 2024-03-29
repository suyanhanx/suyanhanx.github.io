---
title: 日常生活中精密器械面对断电等电力问题的一种解决方案 --- UPS 介绍
tags:
  - hardware
  - intro
categories:
  - hardware
abbrlink: 65399
date: 2022-07-30 09:29:49
toc: true
---
# 日常中会遇到什么样的电力问题？
1. 断电；
2. 雷击等浪涌冲击；
3. 紧急情况下需要续航支持；

那遇到这些问题，有什么解决办法吗？
选用 UPS 就是一种比较方便的解决方案。

<!--more-->

# 什么是 UPS？
不间断电源（或称UPS，即 Uninterruptible Power Supply）是在电网异常（如停电、欠压、干扰或浪涌（涌浪电流））的情况下不间断的为电器负载设备提供后备交流电源，维持电器正常运作的设备。

通常情况下不间断电源被用于维持计算机（尤其是服务器）或交换机等关键性商用设备或精密仪器的不间断运行，防止计算机数据丢失，电话通信网络中断或仪器失去控制。

# UPS 的起源
首个 UPS 专利由约翰 · J · 汉利在1932年11月2日申请，并最终在1934年4月3日获得。
[APPARATUS FOR MAINTAINING AN UNFAIL NG AND UNENTERRUPTED SUPPLY OF ELECTRICAL ENERGY](https://patentimages.storage.googleapis.com/eb/5e/df/208b89f013b7e9/US1953602.pdf)

UPS在其发展初期，仅被视为一种备用电源。后来，由于电压浪涌、电压尖峰、电压瞬变、电压跌落、持续过压或者欠压甚至电压中断等电网质量问题，会使计算机等设备的电子系统受到干扰，造成敏感元件受损、信息丢失等严重后果，引起巨大的经济损失。
因此，UPS日益受到重视，并逐渐发展成具备稳压、稳频、滤波、抗电磁和射频干扰、防电压浪涌等功能的电力保护系统。


# 现代 UPS 的种类
## 1. 离线式/后备式(offline)
1. 平常市电通过旁路直接向负载设备供电。只有在停电时，才通过逆变器将电池能量转换为交流向负载设备提供电力；
2. 当市电正常时，离线式UPS对市电没有任何处理而直接输出至负载设备，因此对市电噪音以及浪涌的抑制能力较差；
3. 特点：
    1. 存在转换时间；
    2. 保护性能最差；
    3. 结构简单、体积小、重量轻、控制容易、成本低。
## 2. 在线交互式(line-interactive)
1. 平常由旁路经变压器输出给负载设备，逆变器此时作为充电器。当断电时逆变器则将电池能量转换为交流电输出给负载设备。
2. 特点：
    1. 具双向性转换器设计，UPS电池回充时间较短；
    2. 存在转换时间；
    3. 控制结构复杂，成本较高；
    4. 保护性能介于在线式与离线式UPS之间，对市电噪音和浪涌的抑制能力较差。
## 3. 在线式/双转换(online/double-conversion)
1. 平常由逆变器输出向负载供电，只有当 UPS 发生故障、过载或过热时才会转为由旁路输出给负载设备；即市电一般情况下是不会直接向负载设备供电的。
2. 特点：
    1. 输出的电力经过UPS的处理，输出电源品质最高；
    2. 无转换时间；
    3. 结构复杂，成本较高；

注：
1. 转换时间：即 UPS 供电由市电切换为内部电池的时间差；
2. 旁路：当 UPS 本身故障时，藉由 UPS 内部的继电器 (Relay) 自动切换至市电，由旁路电路持续供应电力给负载设备，使 UPS 不会因此造成电力中断。[旁路](https://baike.baidu.com/item/%E6%97%81%E8%B7%AF/5310018)

## UPS 的一些特色功能
1. UPS 很安静；
2. 容量只决定于电池有多大，所以某些型号还提供外接电池的功能，让用户自行决定后援电力的储备量；
3. 很多 UPS 除了电源输出外，还设计有用于通讯的 USB 接口，可以通知负载设备自身的状态，让负载设备可以做好准备，或者视 UPS 的电池状态来决定是否关机等等；目前很多 UPS 都会兼容市面上有这种需求的负载设备，链接通讯后就会被识别，甚至如 Mac、NAS 等都不需要安装第三方软件，直接通过操作系统就能管理。

还有一些特别的：

1. [癮觀點：你可能沒想過的面向，UPS追求效率與虛擬化管理](https://www.cool3c.com/article/116027)
2. 据 [@Manjusaka](https://github.com/Zheaoli) 表示，接入 UPS 后，Mac 会调整 SSD 的读写策略。这似乎是一种推测。参考[Apple 对 UPS 的设置文档](https://support.apple.com/guide/mac-help/change-energy-saver-preferences-mchlp1168/mac)

# 怎么挑选 USP
请参考 [2022年1月UPS不间断电源选购指南](https://zhuanlan.zhihu.com/p/257918027)


# 参考文献
1. [UPS-Wikipedia](https://en.wikipedia.org/wiki/Uninterruptible_power_supply)
2. [UPS不间断电源基础知识](https://zhuanlan.zhihu.com/p/102981599)
3. [UPS电源的基本知识](http://www.sohu.com/a/252279186_470046)
4. [更改 Mac 笔记本电脑上的 UPS 偏好设置](https://support.apple.com/zh-cn/guide/mac-help/mchl0f2f4191/12.0/mac/12.0)
