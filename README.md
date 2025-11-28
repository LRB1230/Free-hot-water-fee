# Free-hot-water-fee
关于湖南大众传媒，洗澡水费破解，提供教程
大众的水费实在太贵了，洗一次4块钱，网上的的教程又完全没有关于智校乐的

长沙基本全部是用智校乐，理论全部可行

交流群：https://qm.qq.com/q/cabGZxG88g
# 接下来是原理
水表本质上是无法联网的，水表是通过蓝牙连接手机，手机再发出数据包给服务器。
我们执行的操作是在手机发出数据包的时候拦截下来这个数据包，通过规则替换，替换水费为0

不能使用在黄鸟普通版，没有规则替换，普通版本没有规则替换，而数据包有随机值校验（防止重发）
# 教程
**1.在我的库中下载HttpCanary专业版,并且安装，自行下载mt管理器**
  
**2.安装CA证书**

  （1）打开HttpCanary黄鸟
  
  （2）![Screenshot_2025-11-28-17-03-23-770_com guoshi httpcanary-edit](https://github.com/user-attachments/assets/b4732506-b1fc-4838-9fc1-968863c8bb1c)
  
  （3）![Screenshot_2025-11-28-17-04-30-256_com guoshi httpcanary-edit](https://github.com/user-attachments/assets/b9c28a68-7aab-46ae-a7c3-42414d7061eb)
  
  （4）![Screenshot_2025-11-28-17-05-28-780_com guoshi httpcanary-edit](https://github.com/user-attachments/assets/5eff851f-1ad8-4c6d-9bc9-a486c5f0fb16)
  
  （5）![Screenshot_2025-11-28-17-06-43-797_com guoshi httpcanary-edit](https://github.com/user-attachments/assets/b12496dc-acb7-4143-b0b2-06fc99f44437)
  
  （6）![Screenshot_2025-11-28-17-07-12-488_com guoshi httpcanary-edit](https://github.com/user-attachments/assets/b4b2a7bf-cd3c-4d37-9da3-1d71565204b9)

  （7）打开手机的设置
  
  （8）![b9b33233eb3940c6cb5c5d89f4d09a1e](https://github.com/user-attachments/assets/0bc3ac4a-79f1-4e66-88f3-b0c405e9b552)
  
  （9）![043abab511bf3d14e1614e78634a003c](https://github.com/user-attachments/assets/c5ffe24a-3a67-48de-a9e4-4eefe985d6f4)

  （10）![3cb9cdaf186142d64aac4a2d0c1d6d69](https://github.com/user-attachments/assets/3e23c991-68b9-4058-84b3-cd4f576a6173)

  （11）![096f8586de472134f426b84682bc2d28](https://github.com/user-attachments/assets/5023e255-708e-4a49-a7ce-e48364121ec5)
  
  （12）![9793ed75f8d9d89af03b0ba11fe49a15](https://github.com/user-attachments/assets/40119fc0-8947-4687-af39-6225f7ad6182)

  （13）![b06b310df990b06fb2876dec29e01335](https://github.com/user-attachments/assets/b56d2b90-bb2d-4e5c-91e8-8387f2e64ae0)

  （14）![8f18835a53f9c59f8819ed49489606fa](https://github.com/user-attachments/assets/6b90d0f5-a954-43a8-9e12-6602c6fa0b76)
  
  （15）![00de8bea652ecb74e31943a2e2dbbe53](https://github.com/user-attachments/assets/0c687684-f904-491f-afdc-0a204d9cb285)
  
  （16）![1c7609327a628f5276df37a0c0897466](https://github.com/user-attachments/assets/357f3c35-95ea-43bf-b2c4-4295d55c4437)
  
**3.使用黄鸟，抓取点击"结束洗澡"发出的数据包**

  （0）如果遇到，搜索界面，没有任何软件，也搜索不到，就是没有给与读取应用列表权限，请自行去设置更改
  
  （1）打开HttpCanary黄鸟
  
  （2）![Screenshot_2025-11-28-17-03-23-770_com guoshi httpcanary-edit](https://github.com/user-attachments/assets/1cef63be-44fe-482e-86d3-32ba264abc43)
  
  （3）![f0fb8d43416585a156785c86a2b50379](https://github.com/user-attachments/assets/eae64310-d182-46c7-9ada-52c8bb592788)
  
  （4）![cf73c65c9facf7580e97ef7ebdf1a386](https://github.com/user-attachments/assets/baf5a2ab-381c-470c-8c3c-a1f377d1fcae)
  
  （5）![99e2b2c7f362651a05ceb6fb759ad59a](https://github.com/user-attachments/assets/6247eb9c-98f2-4cf0-b39d-19b707f2fea3)
  
  （6）![50dfc09a91c6312c6097b6fc291f598e](https://github.com/user-attachments/assets/80cc2454-6cff-4e6e-8586-224951630ddb)

  （7）接下来，进入智校乐，进入洗澡模式开始洗澡并结束洗澡，再返回HttpCanary黄鸟，点击下面绿色的纸飞机图标，结束抓包
  
   ![Screenshot_2025-11-28-19-02-31-57_265eefe1b4d950c](https://github.com/user-attachments/assets/227d9dc7-f97b-48ba-8a6d-9c3b8759b45a)
 
**4.找到具体是哪一个数据包发出洗了多少钱**

  （1）![IMG_20251128_190813](https://github.com/user-attachments/assets/6766891f-e513-44dc-8429-c258a67b2bde)

**5.重写，创建规则，完成**

  (1)长按该数据包

 （2）![Screenshot_2025-11-28-19-02-31-57_265eefe1b4d950c](https://github.com/user-attachments/assets/227d9dc7-f97b-48ba-8a6d-9c3b8759b45a)
 
 （3） ![Screenshot_2025-11-28-19-02-31-57_265eefe1b4d950c](https://github.com/user-attachments/assets/227d9dc7-f97b-48ba-8a6d-9c3b8759b45a)
 
 （4）![IMG_20251128_191959](https://github.com/user-attachments/assets/7fdd4c53-6feb-412c-a25f-97aadfe198c8)
 
 （5）![IMG_20251128_192144](https://github.com/user-attachments/assets/617e4e2f-6178-4de6-ad73-96bf75451916)
 
 （6）点击下面的加号，创建两个这样的
 
 （7）![IMG_20251128_192928](https://github.com/user-attachments/assets/4797bd09-c920-41fa-9b9a-62390a79a48e)
 
 （8）![IMG_20251128_192928](https://github.com/user-attachments/assets/1fa46d05-4871-4126-92f0-6053b71b831f)

 （9）![IMG_20251128_193633](https://github.com/user-attachments/assets/54ffe49a-d9f8-42d4-890f-ebcb3f2cab96)
 
 （10）![IMG_20251128_193817](https://github.com/user-attachments/assets/d4812ae4-e7ce-4b39-889a-21c981f8843a)
**6.重写，创建规则，完成**
# 使用方法
**每次使用，先打开HttpCanary黄鸟，点击下面绿色的纸飞机图标，开始抓包，就可以正常使用智校乐，就会是0元计费了**
# 附加（上面的更改基于大众传媒的水表，其他学校可能没有效果，可以根据下面这些进行一定的更改）
**7.关于个人敏感信息我打成x了**
```
用户身份信息

· accountId=xxxxxx：用户账户ID
· telPhone=xxxxxxxxxxx：用户手机号
· loginCode=xxxxxxxxxxxx：登录会话令牌（MD5格式）

交易信息

· projectId=73：消费项目ID（固定值，可能是洗衣服务）
· upMoney=40：消费金额为40（消费金额0.04）
· accountType=x：账户类型
· protocolType=xxxx：协议类型（xxxx可能表示特定通信协议）

时间与安全

· consumeDate=2511xxxxxx：消费时间（2025年11月xxxxxxxxx)
· randomNumber=xxxxx：随机数（防重放攻击）

系统信息

· version=4.2.6：客户端版本
· phoneSystem=android：操作系统
· signature=：数字签名（为空，安全漏洞）

xfData 详细解析

结构分解：

偏移 十六进制 长度 解析结果 说明

0-1 80 1字节 协议头 固定起始标志

2-3 25 1字节 年(25) 2025年

4-5 11 1字节 月(11) 11月

6-7 xx 1字节 日

8-9 xx 1字节 时

10-11 xx 1字节 分

12-13 xx 1字节 秒

14-21 00000049 4字节 项目ID(73) 0x49 = 73

22-29 xxxxxxxx 4字节 未知 可能是版本或类型

30-37 xxxxxxxx 4字节 账户ID(xxxxx) xxxxx = xxxxx

38-45 xxxxxxxx 4字节 账户类型(x) 与accountType对应

46-53 xxxxxxxx 4字节 未知(xx) 可能与projectId相关

54-61 00001770 4字节 预付款金额or最高消费金额 （6000）6块钱

62-69 00000028 4字节 金额相关(40) 0x28 = 40

70-77 00000028 4字节 金额相关(40) 重复字段

78-85 xxxxxxxx 4字节 时间戳 可能是Unix时间戳

86-93 xxxx 4字节 随机数部分 与randomNumber关联

94-101 000400f0 4字节 设备标识 可能标识终端设备

102-109 000a0000 4字节 命令类型 0x0A = 10，可能表示特定操作

110-117 00000000 4字节 保留字段 全零

118-125 xxxxxxx 4字节 校验数据 可能是CRC32或校验和

126-131 7b9caf 3字节 结束标志 固定结束标记
```

特征

1. 零金额交易：upMoney=40 消费金额
2. 完整时间戳：包含精确到秒的交易时间
3. 设备信息：xfData中包含设备标识和随机数
4. 固定项目：projectId=73 重复出现
5. xfData中间的16进制消费金额 00000028 0x28 = 40

