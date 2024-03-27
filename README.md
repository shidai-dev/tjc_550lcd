## TJC X550 5寸屏幕个人DIY固件
### 此固件仅用作个人学习使用，可能存在诸多问题请友善提出
[参考链接 on7lds NextionDriver](https://github.com/on7lds/NextionDriver "NextionDriver")

[参考链接 g4klx MMDVMHost](https://github.com/g4klx/MMDVMHost "MMDVMHost")

# 参考HMI固件 ”hs9awo“进行开发
仅做了MMDVM主页和DMR页面，其他d-star、p25等没进行开发，本人只有dmr设备用不到

- tjc串口屏如果从双工热点版串口出来只支持9600波特率
- 本项目使用的是自带RTC时钟，时间均是来自屏幕RTC时钟时间，并非串口数据

### 串口相关数据
部分数据比如cpu、mem、disk信息是需要Nextion驱动支持

--- 已打开串行端口 COM10 ----

page MMDVM

MMDVM.status.val=1

dim=20

t0.txt="呼号/DMRID"

t4.txt="呼号"

t5.txt="DMRID"

MMDVM.status.val=17

t30.txt="433.750000"

MMDVM.status.val=20

t32.txt="439.750000"

MMDVM.status.val=21

t20.txt="41.9 �C"

MMDVM.status.val=22 click S0,1

t1.txt="MMDVM IDLE"

MMDVM.status.val=11 click S0,1

t3.txt="eth0:10.119.114.105"

-------------------------------page DMR-----------------------------

dmr分时隙1、时隙2 变量不同

page DMR

MMDVM.status.val=3

-------时隙1----

t1.txt="TGID"//组 ID

t0.txt="1 Listening" // 呼号等

t18.txt=""//呼号

t19.txt=""//姓

t20.txt=""//名

t21.txt=""//地址

t22.txt=""//国家


dim=50   //屏幕亮度

-------时隙2-----

t2.txt="2 N BI3NIA Wu"

t13.txt="BI3NIA"

t14.txt="Wu"

t15.txt="老A"

t16.txt="Shijiazhuang"

t17.txt="China"

MMDVM.status.val=78

t3.txt="TG46003"//组ID
