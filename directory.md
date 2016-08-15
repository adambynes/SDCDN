前言

第一部分 SDDCN基础（60页）
一、	背景知识介绍  
a)	数据中心——前世与今生  
b)	云计算——浪潮之巅  
c)	网络虚拟化——业务对网络的引领  
i.	VLAN与VPN  
ii.	数据中心网络的虚拟化  
iii.	控制平面虚拟化  
iv.	数据平面虚拟化  
d)	SDN——从喊口号到落地  
i.	SDN是个新概念吗？  
ii.	学术界的崛起：OpenFlow  
iii.	SDN≠OpenFlow  
iv.	业界的迷惘  
v.	开源SDN带来的曙光  
vi.	Time for Business  
e)	NFV——运营商的变革决心  
i.	基础设施即软件  
ii.	XaaS：一切即服务  
iii.	与SDN并肩作战  
iv.	vswitch与vrouter  
v.	为网络增值：L4~L7   

二、	软件定义数据中心网络（SDDCN）概述  
a)	再论SDN  
i.	狭义SDN与广义SDN  
ii.	分布式与集中式之争  
iii.	从N到D到S：回归软件本源，微内核与分布式数据库简介  
b)	为什么要用SDN改造数据中心网络？  
i.	大二层：爆炸的东西向流量   
ii.	按需服务：传统网络的阿喀琉斯之踵  
iii.	自动化即王道：与SDN是天作之合  
iv.	基于SDN的云数据中心网络：设计原则  
v.	基于SDN的云数据中心网络：应用场景  
c)	软件定义数据中心互联（SDDCI）与软件定义存储网络（SDSAN）  
i.	SDDCI：冉冉升起的新星  
ii.	SDSAN：仍在探索  
d)	SDDCN关键技术  
i.	Network Edge  
ii.	Network Fabric  
iii.	Network Service  
iv.	Network Security  
v.	Network OAM  
e)	向SDDCN演进  
i.	Overlay：称霸Network Edge  
ii.	SDFabric：Underlay的战争  
iii.	Service Function Chain：与NFV的融合  
iv.	安全与运维：路漫漫其修远兮  

第二部分	SDDCN深入解读——内涵篇（150页）
三、	商用SDDCN简介  
a)	Vmware NSX：软件厂商的开创  
b)	Cisco ACI：硬件厂商的回应  
c)	BigSwitch：颠覆者  
d)	其它商用SDDCN速览  

四、	开源SDDCN进展
a)	Openstack Neutron：生态制定者  
b)	OpenContrail：探索者  
c)	OpenDaylight：领先者  
d)	ONOS：跟随者  

五、	开源SDDCN——设计与实现  
a)	Openstack Neutron设计  
i.	OpenStack网络基础  
ii.	Neutron-Server设计与实现  
iii.	OVS-Agent设计与实现  
iv.	OF-Agent设计  
v.	Midolnet设计    
vi.	DragonFlow设计  
vii.	OVN设计  
viii.	Neutron SFC设计  
ix.	Neutron最新blueprint速览  
b)	OpenContrail  
i.	OpenContrail设计与实现  
c)	OpenDaylight  
i.	OVSDB Netvirt设计与实现  
ii.	OVSDB HWTEP设计与实现  
iii.	VTN设计与实现  
iv.	SFC设计与实现  
d)	ONOS  
i.	ONOSFW设计与实现  
ii.	OpenStack套件设计与实现  
iii.	CORD设计与实现  

六、	开源SDDCN控制——横向测评  
a)	设计架构（vswitch类型、Overlay组网、Underlay可管理性、pipeline、协议、集中/分布、reactive/proactive、虚拟化技术选型、高可用、DB选型、消息中间件、对Neutron API的支持、与Neutron Server的同步机制）  
b)	功能测试
i.	VPC基本功能（租户内部L2/L3通信、多租户隔离、FloatingIP、SNAT、安全组策略、虚拟机迁移网络策略自动跟随）  
ii.	VPC流量优化（ARP、DHCP、未知单播、DVR）  
iii.	高级服务（防火墙、负载均衡、VPN）  
iv.	服务链  
v.	服务质量（虚拟机限速、租户限速与带宽保障）  
vi.	可用性（DB集群、控制器灾备、控制器扩容、数据平面逃生机制、设备故障、链路故障）  
c)	性能测试  
i.	数据平面（小包吞吐量、大包吞吐量、CPU、内存、端到端延时、DPDK优化）  
ii.	控制平面（host数量、vSwitch数量、流表数量、PacketIn、FlowMod、ARP）  
iii.	业务平面（Neutron API并发）  

第三部分	SDDCN深入解读——外延篇（60页）
七、	SDDCN与容器网络  
a)	云计算主战场——虚拟机与容器  
b)	容器网络简介  
i.	容器网络概述  
ii.	Docker网络演进  
iii.	容器网络选手速览  
c)	通过OpenStack Kuyrr与Neutron进行集成  

八、	SDDCN 数据平面关键技术  
a)	传统的linux kernel数据平面的内容
i.	LB  
ii.	Softirq tasklet NAPI  
b)	SDDCN提出的挑战  
i.	高吞吐 低延时  
ii.	虚拟化网络  
iii.	网络空间的隔离  
c)	SDDCN虚拟化网络的实现  
i.	SR IOV  
ii.	Front end back end VHOST and virtio-net  
iii.	Network namespace  
iv.	VXLAN  
d)	SDDCN加速的关键技术  
i.	UIO VFIO FUSE CUSE  
ii.	网络协议栈的扁平化  
iii.	基础架构OS的扁平化 unikernel  
iv.	CPU架构的变革对网络包处理的影响  

九、	SDDCN 数据平面开源解决方案
a)	  Netmap & PF ring 数据平面加速的始祖  
b)	  DPDK packet IO 加速的神奇  
c)	  OVS and OVS-DPDK 高效的虚拟交换机  
d)	  VPP 数据平面服务的后起之秀  
e)	  Mtcp networking stack in user space  
f)	  低延时的关键开源软件 openonload  
g)	  SDN数据面编程语言 P4 POF OF-DPA  
h)	  openswitch conntrack and ovs conntrack

第四部分 SDDCN企业部署案例（待定）  
第五部分 SDDCN展望（20页） 
十、	SDDCN未来发展方向  
a)	服务与编排  
i.	SDNO与MANO  
ii.	更多的VNF  
iii.	自动化交付  
b)	安全  
i.	先解决SDN自身的安全问题  
ii.	微分段（Multi-Segment）简介  
iii.	软件定义的数据中心安全  
c)	自动化运维  
i.	Puppet、Chef与Ansible  
ii.	NetCONF与OpenConfig  
iii.	流量可视化  
iv.	端到端故障监测  
v.	故障的自动排查  
d)	异构与超融合  
i.	机架交换  
ii.	光与无线  
iii.	存储网络  
iv.	高性能计算网络  
e)	大数据  
i.	DaaS——更大的时代驱动力  
ii.	SDN serve for Big Data  
iii.	Big Data serve for SDN  

附录
参考资料
与开源社区互动
后记

Need to 
