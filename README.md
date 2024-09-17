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

### 2.1.4 因特网提供的运输服务
![image](https://github.com/user-attachments/assets/ecbf9d59-88db-48ca-9833-5a07fcfb2a8f)
1. TCP服务
   * 面向连接的服务：在应用层数据报文开始流动之前，TCP让客户和服务器互相交换运输层控制信息。这个所谓的握手过程提醒客户和服务器，让它们为大量分组的到来做好准备。在握手阶段后，一个TCP连接（TCP connection）就在两个进程的套接字之间建立了。这条连接是全双工的，即连接双方的进程可以在此连接上同时进行报文收发。当应用程序结束报文发送时，必须拆除该连接。
   * 可靠的数据传送服务：通信进程能够依靠TCP,无差错、按适当顺序交付所有发送的数据。当应用程序的一端将字节流传进套接字时，它能够依靠TCP将相同的字节流交付给接收方的套接字，而没有字节的丢失和冗余。
2. UDP服务
   * UDP协议提供一种不可靠数据传送服务。进程将一个报文发送进UDP套接字时，UDP协议并不保证该报文将到达接收进程。不仅如此，到达接收进程的报文也可能是乱序到达的。UDP没有包括拥塞控制机制，所以UDP的发送端可以用它选定的任何速率向其下层（网络层）注入数据。（然而，值得注意的是实际端到端吞吐量可能小于该速率，这可能是因为中间链路的带宽受限或因为拥塞而造成的。）

![image](https://github.com/user-attachments/assets/614a8955-567c-4cf7-975d-62d39e059cd3)   

**因特网运输协议所不提供的服务**：因特网能够提供可靠数据传输、安全性。因特网通常能够为时间敏感应用提供满意的服务，但它不能提供任何定时或带宽保证。

### 2.1.5 应用层协议
应用层协议定义了 ：
* 交换的报文类型，例如请求报文和响应报文。
* 各种报文类型的语法，如报文中的各个字段及这些字段是如何描述的。
* 字段的语义，即这些字段中的信息的含义。
* 确定一个进程何时以及如何发送报文，对报文进行响应的规则

### 2.1.6 本书涉及的网络应用
Web 文件传输、电子邮件、目录服务(DNS)、流式视频和P2P。

## 2.2 Web 和 HTTP
### 2.2.1 HTTP 概况
HTTP使用TCP作为它的支撑运输协议，HTTP是一个无状态协议(stateless protocol)。

### 2.2.2 非持续连接和持续连接
1. 采用非持续连接的HTTP：每次请求完都会断开
2. 采用持续连接的HTTP：会复用链接

### 2.2.3 HTTP报文格式
1. HTTP请求报文
<img width="300" alt="image" src="https://github.com/user-attachments/assets/aa69bae3-9e3e-46d7-9567-ae8a05f7a050">   
<br/>
<img width="400" alt="image" src="https://github.com/user-attachments/assets/43df06e0-141e-409a-9d85-f25eba6ed7e5">       

2. HTTP响应报文
<img width="300" alt="image" src="https://github.com/user-attachments/assets/e1e84302-044c-4e74-80a3-f71798f94b3c">   
<br/>
<img width="400" alt="image" src="https://github.com/user-attachments/assets/55b33fe7-1232-4df6-9d3a-240d241dbe6a">    

### 2.2.4用户与服务器的交互：cookie
cookie技术有4个组件：
1. 在HTTP响应报文中的一个cookie首部行；
2. 在HTTP请求报文中的一个cookie首部行；
3. 在用户端系统中保留有一个cookie文件，并由用户的浏览器进行管理；
4. 位于Web站点的一个后端数据库。

<img width="500" alt="image" src="https://github.com/user-attachments/assets/b6aa5622-5e81-4256-a310-a95a5ff524a1">  

### 2.2.5 Web缓存
局域网内的web缓存器：在局域网安装，局域网内的浏览器要预先设置指向局域网web缓存器（这样的话感觉用得比较少）。   

<img width="300" alt="image" src="https://github.com/user-attachments/assets/ad256475-aceb-42af-a15c-09400dde0f87">  

装在Internet公网的web缓存器：通过使用**内容分发网络**（Content Distribution Network, CDN） , Web缓存器正在因特网中发挥着越来越重要的作用。

### 2.2.6 条件GET方法
首先，一个代理缓存器（proxycache）代表一个请求浏览器，向某Web服务器发送一个请求报文
```http
GET /fruit/kiwi.gif HTTP/1.1
Host: www.exotiquecuisine.com
```
其次，该Web服务器向缓存器发送具有被请求的对象的响应报文:
```http
HTTP/1.1 200 OK
Date: Sat. 3 Oct 2015 15:39:29
Server: Apache/1.3.0 (Unix)
Last-Modified: Wed, 9 Sep 2015 09:23:24
Content-Type: image/gif
(data data data data data...)
```
下次访问Web服务器，带一个首部行，key为If-modified-since，值为上次返回的Last-Modified返回的值
```http
GET /fruit/kiwi.gif HTTP/1.1
Host: www.exotiquecuisine.com
If-modified-since: Wed, 9 Sep 2015 09:23:24
```
Web服务发现没有改变，返回304和空的body
```http
HTTP/1.1 304 Not Modified
Date: Satf 10 Oct 2015 15:39:29
Server: Apache/1 3 0 (Unix)
(empty entity body)
```

## 2.3 因特网中的电子邮件
<img width="500" alt="image" src="https://github.com/user-attachments/assets/d280b4f7-f238-4371-94a4-31c6025aac90">

### 2.3.1 SMTP
1. Alice调用她的邮件代理程序并提供Bob的邮件地址（例如bob® someschool.edu）,撰写报文，然后指示用户代理发送该报文。
2. Alice的用户代理把报文发给她的邮件服务器，在那里该报文被放在报文队列中。
3. 运行在Alice的邮件服务器上的SMTP客户端发现了报文队列中的这个报文，它就创建一个到运行在Bob的邮件服务器上的SMTP服务器的TCP连接。
4. 在经过一些初始SMTP握手后，SMTP客户通过该TCP连接发送Alice的报文。
5. 在Bob的邮件服务器上，SMTP的服务器端接收该报文。Bob的邮件服务器然后将该报文放入Bob的邮箱中。
6. 在Bob方便的时候，他调用用户代理阅读该报文。
![image](https://github.com/user-attachments/assets/2adad483-b5d1-424d-8ada-e35fa9c0567b)    

![image](https://github.com/user-attachments/assets/c97af875-92f5-4545-a83e-eee520fe63bc)   

**特别地：SMTP 一般不使用中间邮件服务器发送邮件，即使这两个邮件服务器位于地球的两端也是这样**。

### 2.3.2 SMTP与HTTP的对比
1. HTTP主要是一个**拉协议**(pull protocol), SMTP基本上是一个**推协议**(push protocol）。
2. SMTP要求每个报文（包括它们的体）采用7比特ASCII码格式。如果某报文包含了非7比特ASCII字符（如具有重音的法文字符）或二进制数据（如图形文件），则该报文必须按照7比特ASCII码进行编码。HTTP数据则不受这种限制
3. 重要区别是如何处理一个既包含文本又包含图形（也可能是其他媒体类型）的文档。HTTP把每个对象封装到它自己的HTTP响应报文中，而SMTP则把所有报文对象放在一个报文之中。

### 2.3.3 邮件报文格式
注意到下列事实：这些首部行不同于我们在2.3.1节所学到的SMTP命令（即使那里包含了某些相同的词汇,如from和to） 那节中的命令是SMTP握手协议的一部分；本节中考察的首部行则是邮件报文自身的一部分。   
一个经典的报文首部看起来如下：   
```smtp
From: alice@crepes.fr
To: bob@hamburger.edu
Subject: Searching for the meaning of life.
```

### 2.3.4 邮件访问协议
![image](https://github.com/user-attachments/assets/8c72b5ac-fdca-4611-9787-98ac5de9b3c6)

1. POP3：一个极为简单的邮件访问协议
2. IMAP：可以管理邮件和文件夹关系等比较复杂的协议
3. 基于Web的电子邮件：有浏览器作为用户代理

## 2.4 DNS: 因特网的目录服务
### 2.4.1 DNS提供的服务
DNS是：   
1. 一个由分层的DNS服务器（DNS server）实现的分布式数据库；
2. 一个使得主机能够查询分布式数据库的应用层协议。

DNS还提供了一些重要的服务：
* **主机别名**（host aliasing）：有着复杂主机名的主机能拥有一个或者多个别名。
* **邮件服务器别名**（mail server aliasing）：MX记录允许一个公司的邮件服务器和Web服务器使用相同（别名化的）的主机名；
* **负载分配**（load distribution）：因为客户通常总是向IP地址排在最前面的服务器发送HTTP请求报文，所以DNS就在所有这些冗余的Web服务器之间循环分配了负载。

### 2.4.2 DNS工作机理概述
1. 分布式、层次数据库
![image](https://github.com/user-attachments/assets/2a1c2f4f-89ec-400c-a109-f401b34dc084)
* 根DNS服务器
* 顶级域(DNS)服务器
* 权威DNS服务器


![image](https://github.com/user-attachments/assets/a274ca62-21a3-4ee7-9a06-8a22ef57f7d8)

2. DNS缓存
DNS服务可以缓存域名解析到本地存储器而不必每次都要请求查询。缓存通常2天过期时间。

### 2.4.3 DNS记录和报文
了资源记录(Resource Record, RR), RR提供了主机名到IP地址的映射。资源记录是一个包含了下列字段的4元组:
```
(Name, Value, Type, TTL)
```
Name和Value的值取决于Type:    
* 如果Type = A,则Name是主机名，Value是该主机名对应的IP地址。因此，一条类型为A的资源记录提供了标准的主机名到IP地址的映射。例如(relay1.bar.foo.com, 145. 37.93. 126, A)就是一条类型 A 记录。
* 如果Type = NS,则Name是个域(如foo. com),而Value是个知道如何获得该域中主机IP地址的权威DNS服务器的主机名。这个记录用于沿着查询链来路由DNS查询。例如(foo.com, dns.foo.com, NS)就是一条类型为NS的记录。
* 如果Type = CNAME，则Value是别名为Name的主机对应的规范主机名。该记录能够向査询的主机提供一个主机名对应的规范主机名，例如(foo.com, relay1.bar.foo.com, CNAME)就是一条 CNAME 类型的记录。
* 如果Type = MX,则Value是个别名为Name的邮件服务器的规范主机名。举例来说，(foo.com, mail.bar.foo.com, MX)就是一条MX记录。MX记录允许邮件服务器主机名具有简单的别名。值得注意的是，通过使用MX记录，一个公司的邮件服务器和其他服务器(如它的Web服务器)可以使用相同的别名。为了获得邮件服务器的规范主机名，DNS客户应当请求一条MX记录；而为了获得其他服务器的规范主机名，DNS客户应当请求CNAME记录。

如果一台DNS服务器是用于某特定主机名的权威DNS服务器，那么该DNS服务器会有一条包含用于该主机名的类型A记录(即使该DNS服务器不是其权威DNS服务器，它也可能在缓存中包含有一条类型A记录)。   

如果服务器不是用于某主机名的权威服务器,那么该服务器将包含一条类型NS记录，该记录对应于包含主机名的域；它还将包括一条类型A记录，该记录提供了在NS记录的Value字段中的DNS服务器的IP地址。举例来说，假设一台edu TLD服务器不是主机gaia.cs.umass.edu的权威DNS服务器，则该服务器将包含一条包括主机cs.umass.edu的域记录，如 (umass.edu, dns.umass.edu, NS)该edu TLD服务器还将包含一条类型A记录,如(dns.umass.edu, 128.119.40.111 A), 该记录将名字dns. umass. edu映射为一个IP地址。   

**1.DNS报文**

DNS只有这两种报文，并且，查询和回答报文有着相同的格式。

![image](https://github.com/user-attachments/assets/1c39dc89-4bb9-49d7-9450-768fe5b6293b)

* 前12个字节是首部区域，其中有几个字段。第一个字段（标识符）是一个16比特的数，用于标识该查询。这个标识符会被复制到对查询的回答报文中，以便让客户用它来匹配发送的请求和接收到的回答。 标志字段中含有若干标志。1比特的“查询/回答”标志位指出报文是查询报文 （0）还是回答报文（1）0当某DNS服务器是所请求名字的权威DNS服务器时，1比特的“权威的”标志位被置在回答报文中。如果客户（主机或者DNS服务器）在该DNS服务器没有某记录时希望它执行递归查询，将设置1比特的“希望递归”标志位。如果该DNS服务器支持递归查询，在它的回答报文中会对1比特的“递归可用”标志位置位。在该首部中，还有4个有关数量的字段，这些字段指出了在首部后的4类数据区域出现的数量。
* 问题区域包含着正在进行的查询信息。该区域包括：①名字字段，包含正在被查询的主机名字；②类型字段，指出有关该名字的正被询问的问题类型，例如主机地址是与一个名字相关联（类型A）还是与某个名字的邮件服务器相关联（类型MX）在来自DNS服务器的回答中，回答区域包含了对最初请求的名字的资源记录。前面讲过每个资源记录中有Type （如A NS CNAME和MX）字段、Value字段和TTL字段。在回答报文的回答区域中可以包含多条RR,因此一个主机名能够有多个IP地址（例如，就像本节前面讨论的冗余Web服务器）。
* 权威区域包含了其他权威服务器的记录。
* 附加区域包含了其他有帮助的记录。例如，对于一个MX请求的回答报文的回答区域包含了一条资源记录，该记录提供了邮件服务器的规范主机名。该附加区域包含一个类型A记录，该记录提供了用于该邮件服务器的规范主机名的IP地址。

**2.在DNS数据库中插入记录**   
注册域名后，需要向注册登记机构提供的你的主dns和备用dns的域名和ip，然后在你的权威dns服务器中加入你的域名配置即可。

## 2.5 P2P文件分发
![image](https://github.com/user-attachments/assets/812daf6a-9268-4489-b161-98152a092536)

## 2.6 视频流和内容分发网
### 2.6.1 因特网视频
通常压缩制作多个版本的视频，比如比特率分别为300kbps 1Mbps和3Mbps用户则能够根据他们当前可用带宽来决定观看哪个版本。
### 2.6.2 HTTP流和DASH
**经HTTP的动态适应性流**(Dynamic Adaptive Streaming over HTTP, DASH): 在DASH中，视频编码为几个不同的版本，其中每个版本具有不同的比特率，对应于不同的质量水平。客户动态地请求来自不同版本且长度为几秒的视频段数据块。当可用带宽量较高时，客户自然地选择来自高速率版本的块；当可用带宽量较低时，客户自然地选择来自低速率版本的块。客户用HTTP GET请求报文一次选择一个不同的块。   
使用DASH后，每个视频版本存储在HTTP服务器中，每个版本都有一个不同的URL HTTP服务器也有一个**告示文件**(manifest file),为每个版本提供了一个URL及其比特率。客户首先请求该告示文件并且得知各种各样的版本。然后客户通过在HTTP GET请求报文中对每块指定一个URL和一个字节范围，一次选择一块。在下载块的同时，客户也测量接收带宽并运行一个速率决定算法来选择下次请求的块。
### 2.6.3 内容分发网
1. CDN操作
当用户主机中的一个浏览器指令检索一个特定的视频（由URL标识）时，CDN必须截获该请求，以便能够：①确定此时适合用于该客户的CDN服务器集群；②将客户的请求重定向到该集群的某台服务器。大多数CDN利用DNS来截获和重定向请求；Netflix由于是自己专用的CDN，搭配自己的客户端，就不需要DNS来决定CDN路由，客户端根据自己的规则自己决定最合适的CDN。
![image](https://github.com/user-attachments/assets/771e612e-9d60-4f7e-9ba9-f76b8042a6c4)

2. 集群选择策略
任何CDN部署，其核心是**集群选择策略**(cluster selection strategy),即动态地将客户定向到CDN中的某个服务器集群或数据中心的机制。一种简单的策略是指派客户到**地理上最为邻近**(geographically closest)的集群。为了基于当前流量条件为客户决定最好的集群，CDN能够对其集群和客户之间的时延和丢包性能执行周期性的**实时测量**(real-time measurement)°

## 2.7 套接字编程：生成网络应用
### 2.7.1 UDP套接字编程
![image](https://github.com/user-attachments/assets/85b501c7-9a5e-4088-adfe-c6d1ca254663)
```python
# UDPClient.py
from socket import *
serverName = 'hostname'
serverPort = 12000
clientSocket = socket(AF_INET, SOCK_DGRAM)
message = raw_input('Input lowercase sentence:')
clientSocket.sendto(message.encode(),(serverName, serverPort))
modifiedMessage, serverAddress = clientSocket.recvfrom(2048)
print(modifiedMessage.decode())
clientSocket.close()
```
```python
UDPServer.py
from socket import *

serverPort = 12000
serverSocket = socket(AF_INET, SOCK_DGRAM)
serverSocket.bind(('', serverPort))
print ("The server is ready to receive...")

while True: 
    message, clientAddress = serverSocket.recvfrom(2048)
    print(clientAddress)
    modifiedMessage = message.decode().upper()
    serverSocket.sendto(modifiedMessage.encode(), clientAddress)
```
### 2.7.2 TCP套接字编程
![image](https://github.com/user-attachments/assets/c44e9363-89c7-4388-bc1b-78527b6419db)    
![image](https://github.com/user-attachments/assets/b396c649-c9d2-4b10-b0e9-3e62b7836ae0)   

```python
# TCPClient.py
from socket import *
serverName = 'servername'
serverPort = 12000
clientSocket = socket(AF_INETr SOCK_STREAM)
clientSocket.connect((serverName, serverPort))
sentence = raw_input('Input lowercase sentence:')
clientsocket.send(sentence.encode())
modifiedSentence = clientsocket.recv(1024)
print('From Server: ', modifiedSentence.decode())
dientSocket.close()
```

```python
# TCPServer.py
from socket import *
serverPort = 12000
serverSocket = socket(AF_INET,SOCK_STREAM)
serverSocket.bind(('', serverPort))
serverSocket.listen(1)
print(FThe server is ready to receive')
while True:
   connectionSocket, addr = serverSocket.accept()
   sentence = connectionsocket.recv(1024).decode()
   capitalizedSentence = sentence.upper()
   connectionsocket.send(capitalizedSentence.encode())
   connectionSocket.close ()
```


## 2.8 小结
在本章中，我们学习了网络应用的概念和实现两个方面。我们学习了被因特网应用普遍采用的客户-服务器模式，并且看到了该模式在HTTP SMTP POP3和DNS等协议中的使用。我们已经更为详细地学习了这些重要的应用层协议以及与之对应的相关应用(Web 文件传输、电子邮件和DNS)O我们也已学习了 P2P体系结构以及它如何应用在许多应用程序中。我们也学习了流式视频，以及现代视频分发系统是如何利用CDN的。对于面向连接的 TCP）和无连接的 UDP）端到端传输服务，我们走马观花般地学习了套接字的使用。至此，我们在分层的网络体系结构中的向下之旅已经完成了第一步

# 运输层
## 3.1 概述和运输层服务
![image](https://github.com/user-attachments/assets/f6ec3dfb-eb20-4cee-b424-81c4d0302c98)
### 3.1.1 运输层和网络层的关系
网络层提供了主机之间的逻辑通信，而运输层为运行在不同主机上的进程之间提供了逻辑通信。

### 3.1.2 因特网运输层概述
UDP和TCP还可以通过在其报文段首部中包括差错检查字段而提供完整性检查。**进程到进程的数据交付**和**差错检查**是两种最低限度的运输层服务，也是UDP所能提供的仅有的两种服务。   

TCP为应用程序提供了几种附加服务。首先，它提供**可靠数据传输**(reliable data transfer)。 通过使用流量控制、序号、确认和定时器，TCP确保正确地、按序地将数据从发送进程交付给接收进程。TCP还提供**拥塞控制**(congestion control)。

## 3.2 多路复用与多路分解
将运输层报文段中的数据交付到正确的套接字的工作称为**多路分解**(demultiplexing) 在源主机从不同套接字中收集数据块，并为每个数据块封装上首部信息(这将在以后用于分解)从而生成报文段，然后将报文段传递到网络层，所有这些工作称为**多路复用**(multiplexing) 

1.无连接的多路复用与多路分解   
一个UDP套接字是由一个二元组全面标识的，该二元组包含一个目的IP地址和一个目的端口号。因此，如果两个UDP报文段有不同的源IP地址和/或源端口号，但具有相同的目的IP地址和目的端口号，那么这两个报文段将通过相同的目的套接字被定向到相同的目的进程。

2.面向连接的多路复用与多路分解   
TCP套接字是由一个四元组（源IP地址, 源端口号，目的IP地址，目的端口号）来标识的。特别与UDP不同的是，两个具有不同源IP地址或源端口号的到达TCP报文段将被定向到两个不同的套接字，除非TCP报文段携带了初始创建连接的请求。

## 3.3 无链接运输：UDP
UDP只是做了运输协议能够做的最少工作。除了复用/分解功能及少量的差错检测外，它几乎没有对IP增加别的东西。   

有许多应用更适合用UDP,原因主要以下几点：   
* 关于发送什么数据以及何时发送的应用层控制更为精细
* 无须连接建立
* 无连接状态
* 分组首部开销小

UDP无拥塞控制可能会导致高丢包率和挤垮TCP会话问题。  

使用UDP的应用是可能实现可靠数据传输的。需要应用做更多的工作。

### 3.3.1 UDP报文段结构
UDP首部只有4个字段，每个字段由两个字节组成。长度字段指示了在UDP报文段中的字节数（首部加数据）。   
![image](https://github.com/user-attachments/assets/847bfae9-a967-4b89-ac6d-b3b3c5b78080)

### 3.3.2 UDP检验和
举例来说，假定我们有下面3个16比特的字：   

![image](https://github.com/user-attachments/assets/c03ec14e-f62c-487c-a702-888058eb5114)    

注意到最后一次加法有溢出，它要被回卷。反码运算就是将所有的0换成1, 所有的1转换成0。因此,该和0100101011000010的反码运算结果是1011010100111101,这就变为了检验和。如果该分组中没有引入差错，则显然在接收方处该和将是111111111111111。如果这些比特之一是0,那么我们就知道该分组中已经出现了差错。   

虽然UDP提供差错检测，但它对差错恢复无能为力。

## 3.4 可靠数据传输原理
### 3.4.1 构造可靠数据传输协议
1. 经完全可靠信道的可靠数据传输：rdt1.0   
   <img width="392" alt="image" src="https://github.com/user-attachments/assets/3b34ee78-87f0-47b7-9c28-38d719ec5f36">
2. 经具有比特差错信道的可靠数据传输：rdt2.0   
基于重传机制的可靠数据传输协议称为**自动重传请求**(Automatic Repeat reQuest, ARQ)协议。重要的是，ARQ协议中还需要另外三种协议功能来处理存在比特差错的情况：
    * 差错检测
    * 接收方反馈
    * 重传
<img src="https://github.com/user-attachments/assets/afeca2f6-f32e-4b80-be2c-6259d6de040a" width="700px"/>

rdt2.0有个严重问题，就是没有考虑ACK或NAK分组受损的可能性。解决这个新问题的一个简单方法（几乎所有现有的数据传输协议中，包括TCP,都采用了这种方法）是在数据分组中添加一新字段，让发送方对其数据分组编号，即将发送数据分组的**序号**（sequence number）放在该字段。于是，接收方只需要检查序号即可确定收到的分组是否一次重传。   

rdt2.1引入了序号：   
<img width="700" alt="image" src="https://github.com/user-attachments/assets/2a37c8eb-0807-4e21-98c3-886c9e5cc1e2">
<img width="700" alt="image" src="https://github.com/user-attachments/assets/df841e7a-6ce7-4ba0-ad9d-3a79dd4b4563">   
 
rdt2.2去掉了NAK，使用ACK带编号来解决：   
<img width="700" alt="image" src="https://github.com/user-attachments/assets/211ad274-80e5-4ffc-8fde-0e6465cc3392">   
<img width="700" alt="image" src="https://github.com/user-attachments/assets/98cc37a9-a782-40db-ad80-2eb4e4644a86">   

3. 经具有比特差错的丢包信道的可靠数据传输：rdt3.0   
应付丢包的方法是重传，还有要确定好超时的时间，多次发送要处理好晚到的ACK   
<img width="700" alt="image" src="https://github.com/user-attachments/assets/bee29840-f366-4158-bc3f-cc9f9a262f7d">  

<img width="661" alt="image" src="https://github.com/user-attachments/assets/18d3e659-19ff-4e44-9bcf-43c1c7087a1b">   

<img width="661" alt="image" src="https://github.com/user-attachments/assets/3dfb2cf1-29de-4e07-a112-e1b60cc0f55a">

### 3.4.2 流水线可靠数据传输协议
流水线的引入能极大提高传输性能。不等待ack就发送下一个分组，需要：   
* 必须增加序号范围，因为每个输送中的分组（不计算重传的）必须有一个唯一的序号，而且也许有多个在输送中的未确认报文。
* 协议的发送方和接收方两端也许不得不缓存多个分组。发送方最低限度应当能缓冲那些已发送但没有确认的分组。如下面讨论的那样，接收方或许也需要缓存那些已正确接收的分组。
* 所需序号范围和对缓冲的要求取决于数据传输协议如何处理丢失、损坏及延时过大的分组。解决流水线的差错恢复有两种基本方法是：**回退N步**(Go Back N,GBN)和**选择重传**(Selective Repeat, SR)

<img width="621" alt="image" src="https://github.com/user-attachments/assets/51a6a34b-3ce8-4d7a-a1c4-15a3df75b9c8">   

### 3.4.3





