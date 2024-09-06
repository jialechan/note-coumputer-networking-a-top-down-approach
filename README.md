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

**OSI模型**   
因特网协议栈不是唯一的协议栈，开放系统互联(OSI)由ISO在70年代提出在先，比因特网协议还早。 

OSI参考模型比因特网协议多了两个层，即**表示层**和**会话层**。   
**表示层**的作用是使通信的应用程序能够解释交换数据的含义。这些服务包括数据压缩和数据加密（它们是自解释的）以及数据描述（这使得应用程序不必担心在各台计算机中表示/存储的内部格式不同的问题）。   
**会话层**提供了数据交换的定界和同步功能，包括了建立检查点和恢复方案的方法。   

因特网缺少这两个层，因为因特网把这两个层的功能实现留给了应用层的开发者自行决定。

### 1.5.2 封装
<img width="700" alt="image" src="https://github.com/user-attachments/assets/c3532a40-b88d-43a4-add5-57fa9de0b35f">   

## 1.6 面对网络攻击
1. 坏家伙能够经因特网将有害程序放入你的计算机中
**僵尸网络**（botnet）大量被控制的主机；**病毒**(virus）是一种需要某种形式的用户交互来感染用户设备的恶意软件。**蠕虫**(worm）是一种无须任何明显用户交互就能进入设备的恶意软件。例如,用户也许运行了一个攻击者能够发送恶意软件的脆弱网络应用程序。
2. 坏家伙能够攻击服务器和网络基础设施   
**拒绝服务攻击**（Denial-of Service(DoS)attack）
   * **弱点攻击**。这涉及向一台目标主机上运行的易受攻击的应用程序或操作系统发送制作精细的报文。该服务器可能停止运行，或者更糟糕的是主机可能崩溃。
   * **带宽洪泛**。攻击者向目标主机发送大量的分组，分组数量之多使得目标的接入链路变得拥塞，使得合法的分组无法到达服务器。
   * **连接洪泛**。攻击者在目标主机中创建大量的半开或全开TCP连接。该主机因这些伪造的连接而陷入困境，并停止接受合法的连接
3. 坏家伙能够嗅探分组
在无线环境，有线广播环境中，比如以太网LAN中，电缆接入技术中，被控制的路由器中，被动的**分组嗅探器**(packet sniffer)能获得分组的副本。防御嗅探器的方法基本都与密码学有关。   
4. 坏家伙能够伪装成你信任的人
将具有虚假源地址的分组注入因特网的能力被称为**IP哄骗**（IP spoofing）,而它只是一个用户能够冒充另一个用户的许多方式中的一种。为了解决这个问题，我们需要采用端点鉴别，即一种使我们能够确信一个报文源自我们认为它应当来自的地方的机制。

## 1.7 计算机网络和因特网的历史
### 1.7.1 分组交换的发展: 1961~1972
### 1.7.2 专用网络和网络互联: 1972~1980
### 1.7.3 网络的激增: 1980~1990
### 1.7.4 因特网爆炸: 20世纪90年代
### 1.7.5 最新发展
* 自2000年开始，我们见证了家庭宽带因特网接入的积极部署
* 高速(54Mbps及更高)公共WiFi网络和经过4G蜂窝电话网的中速(几十Mbps)因特网接入越来越普及
* 社交网络大发展
* 在线服务提供商如谷歌和微软已经广泛部署了自己的专用网络。
* 许多因特网商务公司在“云”（如亚马逊的EC2 谷歌的应用引擎、微软的Azure）中运行它们的应用。

## 1.8小结
我们已经看到构成特别的因特网以及一般的计算机网络的各种硬件和软件。我们从网络的边缘开始，观察端系统和应用程序，以及运行在端系统上为应用程序提供的运输服务。接着我们也观察了通常能够在接入网中找到的链路层技术和物理媒体。然后我们进入网络核心更深入地钻研网络，看到分组交换和电路交换是通过电信网络传输数据的两种基本方法，并且探讨了每种方法的长处和短处。我们也研究了全球性因特网的结构，知道了因特网是网络的网络。我们看到了因特网的由较高层和较低层ISP组成的等级结构，允许该网络扩展为包括数以千计的网络。   

在这个概述性章节的第二部分，我们研究了计算机网络领域的几个重要主题。我们首先研究了分组交换网中的时延、吞吐量和丢包的原因。我们研究得到传输、传播和排队时延以及用于吞吐量的简单定量模型；我们将在整本书的课后习题中多处使用这些时延模型。接下来，我们研究了协议分层和服务模型、网络中的关键体系结构原则，我们将在本书多处引用它们。我们还概述了在今天的因特网中某些更为流行的安全攻击。我们用计算机网络的简要历史结束我们对网络的概述。

# 应用层
## 2.1 应用层协议原理
### 2.1.1 网络应用程序体系结构
* **客户-服务器体系结构**（client-server architecture）：有一个总是打开的主机称为服务器，它服务于来自许多其他称为客户的主机的请求。
* **P2P体系结构**（P2P architecture）：对位于数据中心的专用服务器有最小的（或者没有）依赖。相反，应用程序在间断连接的主机对之间使用直接通信，这些主机对被称为**对等方**。P2P体系结构特性之一是它们的**自扩展性**（self-scalability），由于高度非集中式结构，P2P面临安全性、性能和可靠性等挑战。

### 2.1.2 进程通讯
1. 客户和服务器进程：在一对进程之间的通信会话场景中，发起通信（即在该会话开始时发起与其他进程的联系）的进程被标识为客户，在会话开始时等待联系的进程是服务器。
2. 进程与计算机网络之间的接口：进程通过一个称为套接字(socket)的软件接口向网络发送报文和从网络接收报文。套接字是同一台主机内应用层与运输层之间的接口。由于该套接字是建立网络应用程序的可编程接口，因此套接字也称为应用程序和网络之间的**应用程序编程接口**(Application Programming Interface, API)。应用程序开发者可以控制套接字在应用层端的一切，但是对该套接字的运输层端几乎**没有**控制权。应用程序开发者对于运输层的控制仅限于：①选择运输层协议；②也许能设定几个运输层参数，如最大缓存和最大报文段长度等。
3. 进程寻址：①主机的地址，由**IP地址**标识。②在目的主机中指定接收进程的标识符，由目的地**端口号**标识。

### 2.1.3 可供应用程序使用的运输服务
1. **可靠数据传输**：确保由应用程序的一端发送的数据正确、完全地交付给该应用程序的另一端。如果一个协议提供了这样的确保数据交付服务，就认为提供了**可靠数据传输**(reliable dtatransfer)。
2. **吞吐量**：即运输层协议能够以某种特定的速率提供确保的可用吞吐量。
3. **定时**：即运输层协议也能提供定时保证。例如发送方注入进套接字中的每个比特到达接收方的套接字不迟于100ms。
4. **安全性**：即运输协议能够为应用程序提供一种或多种安全性服务。运输协议能以防该数据以某种方式在这两个进程之间被观察到。运输协议还能提供除了机密性以外的其他安全性服务，包括数据完整性和端点鉴别

