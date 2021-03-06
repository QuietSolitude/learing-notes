# 计算机网络概述Overview

* 网络的三大类
  * 电信网络，有线电视网络和计算机网络。

* 主机（host）：是指与计算机网络相连的计算机。
* 结点（node）：网络中的主机或者交换机或者路由器。
* 链路（link）：网络中链接这些结点的网线和光纤。
* 带宽（bandwidth）：不同链路的传输速度，单位是bit/s或者bps或b/s。

* 计算机网络：是由若干结点（node）和连接这些结点的链路（link）组成的。 
* 互连网（Internet）：计算机网络之间通过路由器互相连接起来。也可以称为网络的网络（network of networks）。
* 互联网：是指超大的互连网，并采用TCP/IP协议作为通信规则。
 
* internet的两个重要的基本特点
  * 连通性（connectivity）：是指互连网可以互相通信。
  * 共享（资源共享）：是指信息共享，软件共享，硬件共享（服务器或者主机共享）。

* 互联网工作方式
  * 边缘部分：是指所有连接在互联网上的主机组成，用户直接使用。
     * 通信方式分为两种：
       * 客户（client）—— 服务器（server）方式（C/S）：是指客户端向服务器发送请求，服务器接收请求后，处理好请求，返回响应。
       * 对等方式（P2P）：没有客户端和服务器之分。可以是客户也可以是服务器。
  * 核心部分：是指大量网络和连接这些网络的路由器组成的，主要为边缘部分提供服务的（提供连通性和交换）。

* ISP（Internet Service Provider）：是指互联网服务提供商。

* 协议：是指网络通信实体之间在数据交换过程中需要遵循的规则或规定。
  * 三要素：
    * 语法（syntax）：指交换信息的格式与结构。
    * 语义（semantics）：是指实体之间交换的信息。
    * 时序（timing）：是指交换信息的顺序以及如何匹配彼此的速度。
* 计算机网络的功能：通过信息交换实现了资源共享。
    * 硬件资源共享、软件资源共享、信息资源共享。

* 计算机网络的分类：
  * 按覆盖范围分类
    * 个域网（Personal Area Network, PAN）：是指个人设备通过无线通信技术构成小范围的网络，实现的个人设备间的数据传输。比如蓝牙。
    * 局域网（Local Area Network, LAN）：是指采用告诉有线或者无线链路连接主机，实现局部范围的数据传输，比如公司或校园。
    * 城域网（Metropolitan Area Network, MAN）：是指覆盖一个城市范围的网络。
    * 广域网（Wide Area Network, WAN）：是指跨越更大的地理空间，可以实现异地城域网或局域网互相。
  
  * 按拓扑结构分类：是指网络中的主机、网络设备间的物理连接关系与布局。
    * 星形拓扑结构：是指主机通过点对点通信链路与中央结点连接，多用于个域网或者局域网。
      * 优点：易于监控与管理，故障诊断与隔离。
      * 缺点：中央结点是网络的瓶颈，一旦故障，全网瘫痪，网络规模受限于中央结点的端口数量。
    * 总线型拓扑结构：是指一条总链路与所有结点连接，结点间的通信均通过总链路，多用于早期的局域网。
      * 优点：结构简单，需要的链路数量少，易于扩展。
      * 缺点：通信范围受限制，故障诊断与隔离较困难，容易产生冲突（如果两个或两个以上同时通过总链路发送数据，就会产生干扰，会导致任何一个结点的数据发送失败）。
    * 环形拓扑结构：是指利用链路将所有结点连接成一个闭环的环，每个结点发送数据会沿着特定的方向绕环一周最后回到发送的结点，该结点负责清除，如果某结点判断是发给自己的，就会复制这个数据。多用于早期的局域网、园区网或城域网。
      * 优点：需要的链路长度短，易于避免冲突。
      * 缺点：某个结点的故障容易引起全网瘫痪，新结点加入或撤出过程比较麻烦，存在等待时间问题。
    * 网状拓扑结构：是结点通过多条链路与其他结点直接连接。如果结点与其他所有结点均有直接链路连接就是完全网状拓扑结构，否则是非完全网状拓扑结构。多用于广域网、核心网。
      * 优点：网络可靠性强，一条或多条链路故障时，网络任然可以联通。
      * 缺点：结构复杂，造价高，选路协议复杂。
    * 树形拓扑结构：是总线型拓扑结构和星形拓扑结构的扩展，多用于局域网。
      * 优点：易于扩展，故障隔离容易。
      * 缺点：对根结点的可靠性能要求高，一旦出现故障可能导致网络大范围无法通信。
    * 混合拓扑结构：是由两种以上简单拓扑结构混合连接而成的，绝大数网络的拓扑结构是混合拓扑结构。
      * 优点：易于扩展，可以构建不同规模网络，并可根据需要优选网络结构。
      * 缺点：结构复杂，管理与维护复杂。
  
  * 按交换方式分类：是指互连的结点之间的数据交换采用的技术。
    * 电路交换网络
    * 报文交换网络
    * 分组交换网络
  
  * 按网络用户属性分类
    * 公用网（Public Network）
    * 私有网（Private Network）