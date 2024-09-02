# 计算机网络和因特网
## 1.1 什么是因特网
回答这个问题有两种方式：其一，我们能够描述因特网的**具体构成**，即构成因特网的基本硬件和软件组件；其二，我们能够根据为分布式应用提供服务的联网**基础设施**来描述因特网。
### 1.1.1 具体构成描述
因特网中的设备可以称为**主机**（host）或**端系统**（endsystem）。端系统通过**通信链路**（communication link）（同轴电缆、铜线、光纤和无线电频谱）和**分组交换机**（packet switch）连接到一起。设备间把数据将**分段**发送，称为**分组**（pakcet），目的端系统将分组装配为初始数据。最常见的分组交换机类型是**路由器**(router)（通常用于网络核心）和**链路层交换机**(link-layer switch)（通常用于接入网）。   
端系统通过**因特网服务提供商**（Internet Service Provider, ISP）接入因特网，包括如本地电缆或电话公司那样的住宅区ISP、公司ISP、大学ISP。   
端系统、分组交换机和其他因特网部件都要运行一系列**协议**（protocol）,这些协议控制因特网中信息的接收和发送。**TCP**（Transmission Control Protocol,传输控制协议）和**IP**（Internet Protocol,网际协议）是因特网中两个最为重要的协议。
**因特网工程任务组**(Internet Engineering Task Force, IETF)主要工作是定义**请求评论**(Request For Comment, RFC)，RFC定义了TCP、IP、HTTP(用于Web)和SMTP (用于电子邮件)等协议。   
<img src="https://github.com/user-attachments/assets/b26bee42-dcf3-4423-8b23-c397964c2ab3" width="400px"/>
### 1.1.2 服务描述
因特网为分布式应用程序提供了基础设施服务：**套接字接口**( socket interface)，该接口规定了运行在一个端系统上的程序请求因特网基础设施向运行在另一个端系统上的特定目的地程序交付数据的方式。
### 1.1.3 什么是协议
**协议**(protocol)定义了在两个或多个通信实体之间交换的报文的格式和顺序，以及报文发送和/或接收一条报文或其他事件所采取的动作。掌握计算机网络领域知识的过程就是理解网络协议的构成、原理和工作方式
的过程。
## 1.2 网路边缘
### 1.2.1 接入网
**接入网**这是指将端系统物理连接到其**边缘路由器**（edge router）的网络。边缘路由器是端系统到任何其他远程端系统的路径上的第一台路由器。   
   
1.家庭接入：DSL 电缆、FTTH 拨号和卫星   
**数字用户线**（Digital Subscriber Line, DSL），住户通常从提供本地电话接入的本地电话公司处获得DSL因特网接入。   
<img src="https://github.com/user-attachments/assets/4159cfe4-d727-430e-8f02-2a2763037050" width="500px"/>   

**电缆因特网接入**（cable Internet access）利用了有线电视公司现有的有线电视基础设施。因为在这个系统中应用了光纤和同轴电缆，所以它经常被称为混合光纤同轴（Hybrid Fiber Coax, HFC）系统。   
<img width="576" alt="image" src="https://github.com/user-attachments/assets/736a5dad-b3f9-4597-b457-ebc295e09d95">   

**光纤到户**(Fiber To The Home, FTTH) 从本地中心局直接到家庭提供了一条光纤路径。直接光纤，从本地中心局到每户设置一根光纤。

从中心局岀来的每根光纤实际上由许多家庭共享，直到相对接近这些家庭的位置，该光纤才分成每户一根光纤：**主动光纤网络**（Active Optical Network, AON)和**被动光纤网络**(Passive Optical Network, PON)   
<img width="576" alt="image" src="https://github.com/user-attachments/assets/005c133b-1d4a-465c-af48-ac327692c8b4">    

**拨号**速度慢，使用的是电话线；**卫星链路**提供1Mbps以上网速。   

2.企业（和家庭）接入：以太网和WiFi
在公司和大学校园以及越来越多的家庭环境中，使用**局域网**(LAN)将端系统连接到边缘路由器。**以太网**是目前最流行的局域网接入技术。   
<img width="362" alt="image" src="https://github.com/user-attachments/assets/9b8680ef-7954-4a11-b5ae-eb839bb0aa41">    

今天许多家庭将宽带住宅接入（即电缆调制解调器或DSL）与廉价的无线局域网技术结合起来，以产生强大的家用网络。  

3.广域无线接入：3G和LTE
3G提供超过1Mbps的速率。LTE (Long-Term Evolution)来源于3G技术，它能够取得超过10Mbps的速率。

### 1.2.2 物理媒体
1. **双绞铜线**：最便宜并且最常用的导引型传输媒体，一直用于电话网。6a类电缆能够达到10Gbps的数据传输速率，距离长达100m。
2. **同轴电缆**：常建议电缆电视系统。为住宅用户提供数十Mbps速率的因特网接入。同轴电缆能被用作导引型共享媒体(shared medium)，产生的模拟信号从发送设备传送到一个或多个接收方。特别是，许多端系统能够直接与该电缆相连，每个端系统都能接收由其他端系统发送的内容。
3. **光纤**：比特速率高达数十甚至数百Gbps。抗干扰，传输距离100km，难窃听。
4. **陆地无线电信道**：一类运行在很短距离（如1米或2米）；另一类运行在局域，通常跨越数十到几百米；第三类运行在广域，跨越数万米。
5. **卫星无线电信道**：同步卫星有280ms信号传播时延；数百Mbps速率。


