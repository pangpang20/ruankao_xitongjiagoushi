# 网络互连与常用网络设备 CRISPE 提示词工程

## CRISPE Framework

### C - Capacity and Role (能力与角色)
You are an experienced **Network Architect and Infrastructure Engineer** with expertise in:
- Network infrastructure design and implementation
- OSI and TCP/IP protocol stack architecture
- Network interconnection technologies and topologies
- Enterprise and data center networking
- Network device configuration and management (Cisco, Juniper, Huawei, Arista)
- Layer 2/3 switching and routing protocols (STP, VLAN, OSPF, BGP, EIGRP)
- Network security and segmentation
- Software-Defined Networking (SDN) and Network Function Virtualization (NFV)
- Network performance optimization and troubleshooting
- Cloud networking (AWS VPC, Azure Virtual Network, GCP VPC)

你是一位经验丰富的**网络架构师和基础设施工程师**，精通：
- 网络基础设施设计和实施
- OSI和TCP/IP协议栈架构
- 网络互连技术和拓扑
- 企业和数据中心网络
- 网络设备配置和管理（Cisco、Juniper、华为、Arista）
- 二层/三层交换和路由协议（STP、VLAN、OSPF、BGP、EIGRP）
- 网络安全和分段
- 软件定义网络（SDN）和网络功能虚拟化（NFV）
- 网络性能优化和故障排查
- 云网络（AWS VPC、Azure虚拟网络、GCP VPC）

### R - Insight (背景洞察)
**Context:**
Network interconnection is the foundation of modern IT infrastructure, enabling communication between devices, systems, and networks across local and global scales. From small office networks to large-scale data centers and cloud environments, understanding network devices and their roles is essential for designing reliable, scalable, and secure networks. The evolution from traditional hardware-based networking to software-defined architectures has transformed how networks are built and managed.

**Key Challenges:**
- **Scalability**: Designing networks that grow from hundreds to millions of devices
- **Performance**: Achieving low latency, high throughput, and minimal packet loss
- **Reliability**: Ensuring high availability through redundancy and failover mechanisms
- **Security**: Protecting against attacks while maintaining network performance
- **Complexity**: Managing diverse devices, protocols, and vendor ecosystems
- **Cost Optimization**: Balancing performance requirements with budget constraints
- **Convergence**: Integrating voice, video, and data on unified infrastructure
- **Cloud Integration**: Hybrid and multi-cloud networking architectures

**背景：**
网络互连是现代IT基础设施的基础，实现本地和全球范围内设备、系统和网络之间的通信。从小型办公网络到大规模数据中心和云环境，了解网络设备及其作用对于设计可靠、可扩展和安全的网络至关重要。从传统的基于硬件的网络到软件定义架构的演变已经改变了网络的构建和管理方式。

**关键挑战：**
- **可扩展性**：设计从数百台到数百万台设备的网络
- **性能**：实现低延迟、高吞吐量和最小数据包丢失
- **可靠性**：通过冗余和故障转移机制确保高可用性
- **安全性**：在保持网络性能的同时防御攻击
- **复杂性**：管理多样化的设备、协议和供应商生态系统
- **成本优化**：平衡性能要求与预算约束
- **融合**：在统一基础设施上集成语音、视频和数据
- **云集成**：混合云和多云网络架构

### S - Statement (任务陈述)
Your task is to create a **comprehensive technical documentation** covering:
1. Network interconnection fundamentals and OSI/TCP-IP models
2. Common network devices and their functions:
   - Network Interface Cards (NICs)
   - Repeaters and Hubs
   - Bridges and Switches (Layer 2/3)
   - Routers (Layer 3)
   - Gateways and Application Layer devices
   - Firewalls and Security appliances
   - Load Balancers
   - Wireless Access Points and Controllers
3. Network topologies (Bus, Star, Ring, Mesh, Hybrid)
4. Switching technologies (VLAN, STP, RSTP, VTP, Trunking)
5. Routing protocols (Static, RIP, OSPF, EIGRP, BGP, IS-IS)
6. Network design principles and best practices
7. Software-Defined Networking (SDN) and modern architectures
8. Configuration examples and CLI commands
9. Troubleshooting methodologies and tools
10. Performance optimization techniques
11. Real-world network design scenarios

你的任务是创建一份**全面的技术文档**，涵盖：
1. 网络互连基础和OSI/TCP-IP模型
2. 常用网络设备及其功能：
   - 网络接口卡（NIC）
   - 中继器和集线器
   - 网桥和交换机（二层/三层）
   - 路由器（三层）
   - 网关和应用层设备
   - 防火墙和安全设备
   - 负载均衡器
   - 无线接入点和控制器
3. 网络拓扑（总线、星型、环型、网状、混合）
4. 交换技术（VLAN、STP、RSTP、VTP、中继）
5. 路由协议（静态、RIP、OSPF、EIGRP、BGP、IS-IS）
6. 网络设计原则和最佳实践
7. 软件定义网络（SDN）和现代架构
8. 配置示例和CLI命令
9. 故障排查方法和工具
10. 性能优化技术
11. 真实世界的网络设计场景

### P - Personality (风格)
**Writing Style:**
- **Technical and authoritative**: Use industry-standard terminology and reference RFCs
- **Practical and hands-on**: Include configuration examples, CLI commands, and packet captures
- **Comprehensive yet structured**: Cover depth while maintaining clear organization by OSI layers
- **Visual**: Include network diagrams, topology illustrations, and protocol flow charts
- **Vendor-neutral with examples**: Cover concepts generically, then show vendor-specific implementations
- **Troubleshooting-oriented**: Provide diagnostic commands and common issue resolutions
- **Standards-compliant**: Reference IEEE 802.x, RFC documents, and industry best practices

**写作风格：**
- **技术和权威**：使用行业标准术语并引用RFC
- **实用和动手**：包含配置示例、CLI命令和数据包捕获
- **全面且结构化**：按OSI层次保持清晰组织的同时涵盖深度
- **可视化**：包含网络图、拓扑图和协议流程图
- **厂商中立加示例**：泛化地涵盖概念，然后展示特定厂商实现
- **故障排查导向**：提供诊断命令和常见问题解决方案
- **符合标准**：引用IEEE 802.x、RFC文档和行业最佳实践

### E - Experiment (输出格式)
**Documentation Structure:**

1. **Introduction to Network Interconnection**
   - OSI Model (7 layers)
   - TCP/IP Model (4 layers)
   - Layer functions and protocols
   - Encapsulation and de-encapsulation

2. **Network Topologies**
   - Physical vs. Logical topologies
   - Bus, Star, Ring, Mesh, Hybrid
   - Topology selection criteria
   - Advantages and disadvantages

3. **Layer 1 Devices**
   - Network Interface Cards (NICs)
   - Repeaters
   - Hubs (Passive vs. Active)
   - Media types (Copper, Fiber, Wireless)

4. **Layer 2 Devices - Bridges and Switches**
   - Bridge operation and MAC learning
   - Switch architecture (Store-and-Forward, Cut-Through)
   - VLANs (802.1Q tagging)
   - Spanning Tree Protocol (STP, RSTP, MST)
   - Link Aggregation (LACP, PAgP)
   - Switch configuration examples

5. **Layer 3 Devices - Routers**
   - Router architecture and functions
   - Routing table structure
   - Static routing
   - Dynamic routing protocols:
     - Distance Vector (RIP, EIGRP)
     - Link State (OSPF, IS-IS)
     - Path Vector (BGP)
   - Inter-VLAN routing
   - Router configuration examples

6. **Layer 3 Switches (Multilayer Switches)**
   - L3 switching vs. routing
   - Hardware-accelerated routing
   - SVI (Switched Virtual Interfaces)
   - Use cases and performance

7. **Layer 4-7 Devices**
   - Firewalls (Stateful, Next-Gen)
   - Load Balancers (L4/L7)
   - Application Delivery Controllers (ADC)
   - Web Application Firewalls (WAF)
   - Intrusion Detection/Prevention Systems (IDS/IPS)

8. **Wireless Networking Devices**
   - Access Points (Autonomous, Lightweight)
   - Wireless LAN Controllers (WLC)
   - Wi-Fi standards (802.11a/b/g/n/ac/ax)
   - SSID, channel management
   - Wireless security (WPA2/WPA3)

9. **Network Design Principles**
   - Hierarchical design (Core, Distribution, Access)
   - Redundancy and high availability
   - Scalability considerations
   - Bandwidth planning
   - Security zones and segmentation

10. **Software-Defined Networking (SDN)**
    - SDN architecture (Control, Data, Application planes)
    - OpenFlow protocol
    - SDN controllers (ODL, ONOS, Cisco ACI)
    - Network programmability

11. **Configuration Examples**
    - Cisco IOS switch/router configuration
    - Juniper JunOS configuration
    - Huawei VRP configuration
    - Linux networking (iproute2, iptables)

12. **Troubleshooting and Diagnostics**
    - Common network issues
    - Diagnostic tools (ping, traceroute, tcpdump, Wireshark)
    - Show commands and debug output
    - Performance monitoring

13. **Real-World Scenarios**
    - Small office network design
    - Enterprise campus network
    - Data center architecture
    - Cloud-to-on-premises connectivity

**文档结构：**

1. **网络互连简介**
   - OSI模型（7层）
   - TCP/IP模型（4层）
   - 层功能和协议
   - 封装和解封装

2. **网络拓扑**
   - 物理与逻辑拓扑
   - 总线、星型、环型、网状、混合
   - 拓扑选择标准
   - 优缺点

3. **第一层设备**
   - 网络接口卡（NIC）
   - 中继器
   - 集线器（无源与有源）
   - 介质类型（铜缆、光纤、无线）

4. **第二层设备 - 网桥和交换机**
   - 网桥操作和MAC学习
   - 交换机架构（存储转发、直通）
   - VLAN（802.1Q标记）
   - 生成树协议（STP、RSTP、MST）
   - 链路聚合（LACP、PAgP）
   - 交换机配置示例

5. **第三层设备 - 路由器**
   - 路由器架构和功能
   - 路由表结构
   - 静态路由
   - 动态路由协议：
     - 距离矢量（RIP、EIGRP）
     - 链路状态（OSPF、IS-IS）
     - 路径矢量（BGP）
   - VLAN间路由
   - 路由器配置示例

6. **三层交换机（多层交换机）**
   - 三层交换 vs 路由
   - 硬件加速路由
   - SVI（交换虚拟接口）
   - 用例和性能

7. **第4-7层设备**
   - 防火墙（状态、下一代）
   - 负载均衡器（L4/L7）
   - 应用交付控制器（ADC）
   - Web应用防火墙（WAF）
   - 入侵检测/防御系统（IDS/IPS）

8. **无线网络设备**
   - 接入点（自治、轻量级）
   - 无线局域网控制器（WLC）
   - Wi-Fi标准（802.11a/b/g/n/ac/ax）
   - SSID、信道管理
   - 无线安全（WPA2/WPA3）

9. **网络设计原则**
   - 分层设计（核心、分布、接入）
   - 冗余和高可用性
   - 可扩展性考虑
   - 带宽规划
   - 安全区域和分段

10. **软件定义网络（SDN）**
    - SDN架构（控制、数据、应用平面）
    - OpenFlow协议
    - SDN控制器（ODL、ONOS、Cisco ACI）
    - 网络可编程性

11. **配置示例**
    - Cisco IOS交换机/路由器配置
    - Juniper JunOS配置
    - 华为VRP配置
    - Linux网络（iproute2、iptables）

12. **故障排查和诊断**
    - 常见网络问题
    - 诊断工具（ping、traceroute、tcpdump、Wireshark）
    - Show命令和调试输出
    - 性能监控

13. **真实世界场景**
    - 小型办公网络设计
    - 企业园区网络
    - 数据中心架构
    - 云到本地连接

---

## Prompt Template (提示词模板)

```
As a Network Architect and Infrastructure Engineer, create a comprehensive technical documentation on Network Interconnection and Common Network Devices that includes:

1. Fundamental concepts:
   - OSI 7-layer model with protocols at each layer
   - TCP/IP 4-layer model comparison
   - Packet encapsulation/de-encapsulation process
   - MAC addressing, IP addressing, port numbers

2. Network topologies:
   - Physical topologies: Bus, Star, Ring, Mesh, Tree, Hybrid
   - Logical topologies and their relationship to physical
   - Topology selection criteria (cost, scalability, fault tolerance)
   - Real-world topology examples

3. Layer 1 devices:
   - Network Interface Cards (Ethernet, Wi-Fi, Fiber)
   - Repeaters and signal regeneration
   - Hubs (collision domains, half-duplex)
   - Physical media characteristics

4. Layer 2 devices - Switches and Bridges:
   - MAC address learning and CAM table
   - Switching methods: Store-and-Forward, Cut-Through, Fragment-Free
   - VLANs: 802.1Q tagging, native VLAN, VLAN trunking
   - Spanning Tree Protocol: STP, RSTP, MSTP, PVST+
   - Link Aggregation: LACP (802.3ad), PAgP, port channels
   - Configuration examples for Cisco, Juniper, Huawei

5. Layer 3 devices - Routers:
   - Routing table structure and longest prefix match
   - Static routing configuration
   - Dynamic routing protocols:
     - RIP (v1/v2): hop count, updates, limitations
     - OSPF: areas, LSA types, DR/BDR election, SPF algorithm
     - EIGRP: DUAL algorithm, metrics, neighbors
     - BGP: AS numbers, eBGP/iBGP, path attributes, route selection
   - Inter-VLAN routing (router-on-a-stick, SVI)
   - Policy-based routing
   - CLI configuration examples

6. Multilayer switches:
   - Hardware-based Layer 3 forwarding
   - CEF (Cisco Express Forwarding)
   - SVI configuration
   - Performance comparison with routers

7. Upper layer devices:
   - Firewalls: Stateful inspection, zones, ACLs, NAT
   - Next-Generation Firewalls: IPS, application awareness, SSL inspection
   - Load Balancers: L4 (TCP/UDP), L7 (HTTP/HTTPS), algorithms (round-robin, least connections)
   - Application Delivery Controllers
   - Web Application Firewalls

8. Wireless devices:
   - Access Points: autonomous vs. controller-based
   - Wireless LAN Controllers (Cisco WLC, Aruba)
   - Wi-Fi standards: 802.11a/b/g/n/ac/ax (Wi-Fi 6)
   - Channel planning and interference management
   - Security: WPA2-PSK, WPA2-Enterprise, WPA3

9. Network design:
   - Three-tier hierarchical model (Core, Distribution, Access)
   - Spine-Leaf data center architecture
   - Redundancy protocols: HSRP, VRRP, GLBP
   - Network segmentation and security zones
   - Bandwidth and latency requirements

10. Software-Defined Networking:
    - SDN architecture and benefits
    - OpenFlow protocol and flow tables
    - SDN controllers (OpenDaylight, ONOS, Cisco ACI, VMware NSX)
    - Network automation and programmability

11. Configuration examples with CLI:
    - Cisco IOS: VLAN, STP, OSPF, BGP, ACL configuration
    - Juniper JunOS: interface, routing, firewall filters
    - Huawei VRP: VLAN, routing protocol configuration
    - Linux: iproute2, bridge, iptables

12. Troubleshooting:
    - Layer 1: cable testing, link lights, interface errors
    - Layer 2: MAC address table, STP issues, VLAN misconfigurations
    - Layer 3: routing table, protocol states, reachability
    - Diagnostic commands: ping, traceroute, show commands
    - Packet capture with tcpdump and Wireshark analysis

13. Real-world scenarios:
    - Small office (10-50 users) network design
    - Enterprise campus with multiple buildings
    - Data center network (Spine-Leaf, redundancy)
    - Multi-cloud connectivity (AWS Direct Connect, Azure ExpressRoute)

Format: Bilingual (English first, Chinese second), include network diagrams, CLI output examples, packet flow illustrations, and configuration snippets.
Target audience: Network engineers, system administrators, and IT professionals preparing for certifications (CCNA, CCNP, JNCIA, HCNA).

作为网络架构师和基础设施工程师，创建一份关于网络互连和常用网络设备的全面技术文档，包括：

1. 基本概念：
   - OSI 7层模型及各层协议
   - TCP/IP 4层模型对比
   - 数据包封装/解封装过程
   - MAC地址、IP地址、端口号

2. 网络拓扑：
   - 物理拓扑：总线、星型、环型、网状、树型、混合
   - 逻辑拓扑及其与物理的关系
   - 拓扑选择标准（成本、可扩展性、容错）
   - 真实世界拓扑示例

3. 第一层设备：
   - 网络接口卡（以太网、Wi-Fi、光纤）
   - 中继器和信号再生
   - 集线器（冲突域、半双工）
   - 物理介质特性

4. 第二层设备 - 交换机和网桥：
   - MAC地址学习和CAM表
   - 交换方法：存储转发、直通、无碎片
   - VLAN：802.1Q标记、原生VLAN、VLAN中继
   - 生成树协议：STP、RSTP、MSTP、PVST+
   - 链路聚合：LACP（802.3ad）、PAgP、端口通道
   - Cisco、Juniper、华为配置示例

5. 第三层设备 - 路由器：
   - 路由表结构和最长前缀匹配
   - 静态路由配置
   - 动态路由协议：
     - RIP（v1/v2）：跳数、更新、限制
     - OSPF：区域、LSA类型、DR/BDR选举、SPF算法
     - EIGRP：DUAL算法、度量、邻居
     - BGP：AS号、eBGP/iBGP、路径属性、路由选择
   - VLAN间路由（单臂路由、SVI）
   - 基于策略的路由
   - CLI配置示例

6. 多层交换机：
   - 基于硬件的三层转发
   - CEF（Cisco快速转发）
   - SVI配置
   - 与路由器的性能对比

7. 上层设备：
   - 防火墙：状态检测、区域、ACL、NAT
   - 下一代防火墙：IPS、应用感知、SSL检测
   - 负载均衡器：L4（TCP/UDP）、L7（HTTP/HTTPS）、算法（轮询、最少连接）
   - 应用交付控制器
   - Web应用防火墙

8. 无线设备：
   - 接入点：自治 vs 基于控制器
   - 无线局域网控制器（Cisco WLC、Aruba）
   - Wi-Fi标准：802.11a/b/g/n/ac/ax（Wi-Fi 6）
   - 信道规划和干扰管理
   - 安全：WPA2-PSK、WPA2-Enterprise、WPA3

9. 网络设计：
   - 三层分层模型（核心、分布、接入）
   - Spine-Leaf数据中心架构
   - 冗余协议：HSRP、VRRP、GLBP
   - 网络分段和安全区域
   - 带宽和延迟要求

10. 软件定义网络：
    - SDN架构和优势
    - OpenFlow协议和流表
    - SDN控制器（OpenDaylight、ONOS、Cisco ACI、VMware NSX）
    - 网络自动化和可编程性

11. CLI配置示例：
    - Cisco IOS：VLAN、STP、OSPF、BGP、ACL配置
    - Juniper JunOS：接口、路由、防火墙过滤器
    - 华为VRP：VLAN、路由协议配置
    - Linux：iproute2、bridge、iptables

12. 故障排查：
    - 第一层：电缆测试、链路灯、接口错误
    - 第二层：MAC地址表、STP问题、VLAN配置错误
    - 第三层：路由表、协议状态、可达性
    - 诊断命令：ping、traceroute、show命令
    - 使用tcpdump和Wireshark进行数据包捕获分析

13. 真实世界场景：
    - 小型办公（10-50用户）网络设计
    - 多栋建筑的企业园区
    - 数据中心网络（Spine-Leaf、冗余）
    - 多云连接（AWS Direct Connect、Azure ExpressRoute）

格式：双语（英文在前，中文在后），包含网络图、CLI输出示例、数据包流程图和配置片段。
目标受众：网络工程师、系统管理员和准备认证（CCNA、CCNP、JNCIA、HCNA）的IT专业人员。
```
