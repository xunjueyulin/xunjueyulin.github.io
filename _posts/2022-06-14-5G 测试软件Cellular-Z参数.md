---
title:  "5G 测试软件Cellular-Z参数"
date:   2022-06-14 10:44:00
categories: [Communications]
tags: [Network]
---


MCC，Mobile Country Code，移动国家代码（中国的为460）；在该区域内，有共同的编码方法及路由规划，有一个移动交换中心控制区域称为MSC业务区，一个MSC区包含一个或多个位置区。

MNC，Mobile Network Code，移动网络号码（中国移动为0，中国联通为1，中国电信为2）； 

LAC，Location Area Code，位置区域码；最大可以等同于一个msc区，最小可以等同为一个小区的覆盖范围，是对用户发起寻呼的时候的区域，一般是若干个相邻基站的覆盖区域的总和。

CID，Cell Identity，基站编号；

BSSS，Base station signal strength，基站信号强度。

CI：小区识别(Cell Identity)，为了唯一地表示GSMPLMN中的每个小区，网络运营者需分配给网络中所有的小区，即：小区识别(CI)，小区识别(CI)与位置区识别码(LAC)结合，用于识别网络中的每个BTS（基站收发信站点）及其覆盖的小区
TAC：IMEI码的前六位数字即TAC码。TAC码代表了手机的型号
IMEI：（International Mobile Equipment Identity，移动设备国际识别码，又称为国际移动设备标识）由15位数字组成，是手机的唯一识别号码。

RSRP（Reference Signal ReceivedPower参考信号接收功率）：小区下行公共导频在测量带宽内功率的线性值（每个RE上的功率），当存在多根接收天线时，需要对多根天线上的测量结果进行比较，上报值不低于任何一个分支对应的RSRP值，max(RSRP00,RSRP01)。即为信号功率S。反映当前信道的路径损耗强度，用于小区覆盖的测量和小区选择/重选和切换。
取值范围：-44~-140dBm,值越大越好

RS-SINR（Signal to InterferenceNoiseRatio信干噪比）：UE探测带宽内的参考信号功率与干扰噪声功率的比值，即为S/(I+N)，其中信号功率为CRS的接收功率，I+N为参考信号上非服务小区、相邻信道干扰和系统内部热噪声功率总和。反映当前信道的链路质量，是衡量UE性能参数的一个重要指标。
取值范围：0~30 ，值越大越好

RSRQ(Reference Signal ReceivedQuality参考信号接收质量)：M * RSRP/RSSI，其中M为RSSI测量带宽内的RB数，即为系统带宽内的RB总数。反映和指示当前信道质量的信噪比和干扰水平。为了使测量得到的RSRQ为负值，与RSRP保持一致，因此RSRP定义的是单个RE上的信号功率，RSSI定义的是一个OFDM符号上所有RE的总接收功率。
取值范围：-3~-19.5 ，值越大越好

RSSI（Received Signal StrengthIndicator接收信号强度指示)：UE探测带宽内一个OFDM符号所有RE上的总接收功率（若是20M的系统带宽，当没有下行数据时，则为200个导频RE上接收功率总和，当有下行数据时，则为1200个RE上接收功率总和），包括服务小区和非服务小区信号、相邻信道干扰，系统内部热噪声等。即为总功率S+I+N，其中I为干扰功率，N为噪声功率。反映当前信道的接收信号强度和干扰程度。
