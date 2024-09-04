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
<img width="500" alt="image" src="https://github.com/user-attachments/assets/736a5dad-b3f9-4597-b457-ebc295e09d95">   

**光纤到户**(Fiber To The Home, FTTH) 从本地中心局直接到家庭提供了一条光纤路径。直接光纤，从本地中心局到每户设置一根光纤。

从中心局岀来的每根光纤实际上由许多家庭共享，直到相对接近这些家庭的位置，该光纤才分成每户一根光纤：**主动光纤网络**（Active Optical Network, AON)和**被动光纤网络**(Passive Optical Network, PON)   
<img width="500" alt="image" src="https://github.com/user-attachments/assets/005c133b-1d4a-465c-af48-ac327692c8b4">    

**拨号**速度慢，使用的是电话线；**卫星链路**提供1Mbps以上网速。   

2.企业（和家庭）接入：以太网和WiFi
在公司和大学校园以及越来越多的家庭环境中，使用**局域网**(LAN)将端系统连接到边缘路由器。**以太网**是目前最流行的局域网接入技术。   
<img width="500" alt="image" src="https://github.com/user-attachments/assets/9b8680ef-7954-4a11-b5ae-eb839bb0aa41">    

今天许多家庭将宽带住宅接入（即电缆调制解调器或DSL）与廉价的无线局域网技术结合起来，以产生强大的家用网络。  

3.广域无线接入：3G和LTE
3G提供超过1Mbps的速率。LTE (Long-Term Evolution)来源于3G技术，它能够取得超过10Mbps的速率。

### 1.2.2 物理媒体
1. **双绞铜线**：最便宜并且最常用的导引型传输媒体，一直用于电话网。6a类电缆能够达到10Gbps的数据传输速率，距离长达100m。
2. **同轴电缆**：常建议电缆电视系统。为住宅用户提供数十Mbps速率的因特网接入。同轴电缆能被用作导引型共享媒体(shared medium)，产生的模拟信号从发送设备传送到一个或多个接收方。特别是，许多端系统能够直接与该电缆相连，每个端系统都能接收由其他端系统发送的内容。
3. **光纤**：比特速率高达数十甚至数百Gbps。抗干扰，传输距离100km，难窃听。
4. **陆地无线电信道**：一类运行在很短距离（如1米或2米）；另一类运行在局域，通常跨越数十到几百米；第三类运行在广域，跨越数万米。
5. **卫星无线电信道**：同步卫星有280ms信号传播时延；数百Mbps速率。

## 1.3 网络核心
通过网络链路和交换机移动数据有两种基本方法：分组交换（packet switching）和电路交换（circuit switching）。
### 1.3.1 分组交换
1. **存储转发传输**：在交换机能够开始向输岀链路传输该分组的第一个比特之前，必须接收到整个分组。
2. **排队时延和分组丢失**：对于每条相连的链路，该分组交换机具有一个输出缓存（output buffer,也称为输出队列（output queue））。因此，除了存储转发时延以外，分组还要承受输岀缓存的**排队时延**（queuing delay）。因为缓存空间的大小是有限的，一个到达的分组可能发现该缓存已被其他等待传输的分组完全充满了。在此情况下，将出现分组**丢失（丢包）**（packet loss），到达的分组或已经排队的分组之一将被丢弃。
3. **转发表和路由选择协议**：每台路由器具有一个**转发表**(forwarding table)，用于将目的地址(或目的地址的一部分)映射成为输岀链路。你因特网具有一些特殊的**路由选择协议**（routing protocol）,用于自动地设置路由的转发表。

<img width="500" alt="image" src="https://github.com/user-attachments/assets/e700f3b6-5651-403e-9659-ed900e56842a"> 

### 1.3.2 电路交换
电路使用的是**端到端连接**（end to-end connection），在端系统间通信会话期间，**预留**了端系统间沿路径通信所需要的资源（缓存，链路传输速率）。链路中的电路是通过**频分复用** (Frequency- Division Multiplexing, FDM )或**时分复用**（Time-Division Multiplexing, TDM）来实现的。

<img width="500" alt="image" src="https://github.com/user-attachments/assets/0467a69d-5e69-4835-bfd9-103749b7b0d5">    

**分组交换与电路交换的对比**：分组交换提供更好的带宽共享、更简单，更高效，成本更低；电路交换更适合实时服务(电话和视频会议)，但代价可能有点高。目前趋势向分组交换转。

### 1.3.3 网络的网络
今天的因特网是一个网络的网络，其结构复杂，由十多个第一层ISP和数十万个较低层ISP组成。ISP覆盖的区域多种多样，有些跨越多个大洲和大洋，有些限于狭窄的地理区域。较低层的ISP与较高层的ISP相连，较高层ISP彼此互联。用户和内容
提供商是较低层ISP的客户，较低层ISP是较高层ISP的客户。近年来，主要的内容提供商也已经创建自己的网络，直接在可能的地方与较低层ISP互联。   

<img width="500" alt="image" src="https://github.com/user-attachments/assets/970fde9a-7c53-4d92-a508-17e91a655dc0">    

## 1.4 分组交换网络中的时延、丢包和吞吐量
### 1.4.1 分组交换网中的时延概述
1. **处理时延**
检查分组首部和决定将该分组导向何处所需要的时间是**处理时延**的一部分。高速路由器的处理时延通常是**微秒**或更低的数量级。在这种节点处理之后，路由器将该分组引向通往路由器B链路之前的队列。
2. **排队时延**
在队列中，当分组在链路上等待传输时，它经受排队时延。实际的排队时延可以是**毫秒到微秒量**级。
3. **传输时延**
将所有分组的比特推向链路(即传输，或者说发射)所需要的时间。分组长度除以链路带宽。实际的传输时延通常在**毫秒到微秒量**级。
4. **传播时延**
等于或略小于光速。在广域网中，传播时延为**毫秒**量级。

**传输时延和传播时延的比较**: 传输时延是路由器推出分组所需要的时间，它是**分组长度**和**链路传输速率**的函数，而与两台路由器之间的**距离**无关。另一方面，传播时延是一个比特从一台路由器传播到另一台路由器所需要的时间，它是两台路由器之间**距离**的函数，而与**分组长度**或**链路传输速率**无关。

### 1.4.2 排队时延和丢包
随着流量强度接近于1,平均排队时延迅速增加。该强度的少量增加将导致时延大比例增加。   
![image](https://github.com/user-attachments/assets/60d8103d-6c51-487c-9e21-36fb5b2a7dbf)   

**丢包**：当到达分组发现一个满的队列，由于没有地方存储这个分组，路由器将丢弃(drop)该分组。丢失的分组可能基于端到端的原则重传，以确保所有的数据最终从源传送到了目的地。

### 1.4.3 端到端时延
1. Traceroute：观察链路中源到各个路由的时延。
2. 端系统、应用程序和其他时延：
      * 共享媒体（例如在WiFi或电缆调制解调器情况下）传输分组的端系统可能有意地延迟它的传输，把这作为它与其他端系统共享媒体的协议的一部分；
      * 是媒体分组化时延，这种时延出现在IP语音 VoIP）应用中。在VoIP中，发送方在向因特网传递分组之前必须首先用编码的数字化语音填充一个分组。

### 1.4.4 计算机网络的吞吐量
如果没有共享链路，那么吞吐量约等于最小链路的传输速率；有共享带宽的情况，取决于共享链路的实际实时情况（受网络繁忙情况影响）。

## 1.5 协议层次及服务模型
### 1.5.1 分层的体系结构
![image](https://github.com/user-attachments/assets/d29f858d-7001-4c1d-955b-aaf7c97f31aa)   

**因特网协议栈**   
1. **应用层**：应用层是网络应用程序及它们的应用层协议存留的地方。因特网的应用层包括许多协议，例如HTTP （它提供了 Web文档的请求和传送）、SMTP （它提供了电子邮件报文的传输）和FTP （它提供两个端系统之间的文件传
送）、DNS（域名解析）。应用层协议分布在多个端系统上，而一个端系统中的应用程序使用协议与另一个端系统中的应用程序交换信息分组。我们把这种位于应用层的信息分组称为**报文**(message）
2. **运输层**：因特网的运输层在应用程序端点之间传送应用层报文。在因特网中，有两种运输协议，即**TCP**和**UDP**,利用其中的任一个都能运输应用层报文。TCP向它的应用程序提供了面向连接的服务。这种服务包括了应用层报文向目的地的**确保传**递和**流量控制**（即发送方/接收方速率匹配）。TCP也将长报文划分为短报文，并提供**拥塞控制**机制，因此当网络拥塞时，源抑制其传输速率。UDP协议向它的应用程序提供无连接服务。这是一种不提供不必要服务的服务，没有可靠性，没有流量控制，也没有拥塞控制。运输层的分组称为**报文段** (segment)。
3. **网络层**：因特网的网络层负责将称为**数据报**（datagram）的网络层分组从一台主机移动到另一台主机。在一台源主机中的因特网运输层协议（TCP或UDP）向网络层递交运输层报文段和目的地址，就像你通过邮政服务寄信件时提供一个目的地址一样。因特网的网络层包括著名的**网际协议IP**,该协议定义了在数据报中的各个字段以及端系统和路由器如何作用于这些字段。IP仅有一个，所有具有网络层的因特网组件必须运行IP。因特网的网络层也包括决定路由的路由选择协议，它根据该路由将数据报从源传输到目的地。尽管网络层包括了网际协议和一些**路由选择**协议，但通常把它简单地称为IP层，这反映了IP是将因特网连接在一起的黏合剂这样的事实。
4. **链路层**：由链路层提供的服务取决于该链路的特定链路层协议。例如，某些协议基于链路提供可靠传递，从传输节点跨越一条链路到接收节点。值得注意的是，这种可靠的传递服务不同于TCP的可靠传递服务，TCP提供从一个端系统到另一个端系统的可靠交付。链路层的例子包括以太网、WiFi和电缆接入网的**DOCSIS**协议。因为数据报从源到目的地传送通常需要经过几条链路，一个数据报可能被沿途不同链路上的不同链路层协议处理。例如，一个数据报可能被一段链路上的以太网和下一段链路上的**PPP**所处理。网络层将受到来自每个不同的链路层协议的不同服务。把链路层分组称为**帧**(frame）
5. **物理层**：将帧中的一个个比特从一个节点移动到下一个节点。在这层中的协议仍然是链路相关的，并且进一步与该链路（例如，双绞铜线、单模光纤）的实际传输媒体相关。例如，以太网具有许多物理层协议：一个是关于双绞铜线的，另一个是关于同轴电缆的，还有一个是关于光纤的，等等。在每种场合中，跨越这些链路移动一个比特是以不同的方式进行的。

