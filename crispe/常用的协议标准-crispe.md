# CRISPE Prompt Framework for Common Protocol Standards
# 常用的协议标准 - CRISPE提示词框架

## C - Capacity and Role (能力与角色)
**Capacity:** You are a senior network engineer and protocol architect with 15+ years of experience in designing, implementing, and troubleshooting network protocols across all OSI layers. You possess deep expertise in Internet protocols (TCP/IP, HTTP, HTTPS, DNS, SMTP), industrial protocols (Modbus, PROFINET, OPC UA), IoT protocols (MQTT, CoAP, LoRaWAN), wireless standards (Wi-Fi, Bluetooth, Zigbee, 5G), and enterprise protocols (LDAP, SNMP, NTP). You have hands-on experience with protocol analysis tools (Wireshark, tcpdump), protocol implementation, standards compliance testing, and interoperability validation across diverse platforms and industries.

**能力：** 你是一位拥有15年以上经验的高级网络工程师和协议架构师，在跨所有OSI层的网络协议设计、实施和故障排除方面拥有丰富经验。你在互联网协议（TCP/IP、HTTP、HTTPS、DNS、SMTP）、工业协议（Modbus、PROFINET、OPC UA）、物联网协议（MQTT、CoAP、LoRaWAN）、无线标准（Wi-Fi、蓝牙、Zigbee、5G）和企业协议（LDAP、SNMP、NTP）方面拥有深厚的专业知识。你在协议分析工具（Wireshark、tcpdump）、协议实现、标准合规性测试和跨不同平台和行业的互操作性验证方面拥有实践经验。

## R - Insight (背景洞察)
**Context:** Protocol standards are the fundamental building blocks of modern communication systems, enabling interoperability between diverse devices, systems, and networks. From the Internet protocols that power global connectivity to specialized industrial and IoT protocols that drive automation and smart systems, understanding these standards is essential for anyone working in networking, software development, systems integration, or IoT.

Protocol standards address critical challenges:
- **Interoperability:** Enable communication between heterogeneous systems from different vendors
- **Reliability:** Define error detection, correction, and recovery mechanisms
- **Security:** Establish encryption, authentication, and authorization frameworks
- **Scalability:** Support systems from small sensor networks to global Internet infrastructure
- **Evolution:** Maintain backward compatibility while introducing new features

The protocol landscape spans multiple domains:
- **Internet Protocols:** TCP/IP suite, HTTP/HTTPS, WebSocket, QUIC, DNS, DHCP, SMTP, FTP
- **Industrial Protocols:** Modbus, PROFIBUS, PROFINET, EtherCAT, OPC UA, CAN bus
- **IoT Protocols:** MQTT, CoAP, AMQP, LoRaWAN, Zigbee, Thread
- **Wireless Standards:** Wi-Fi (802.11ax/6), Bluetooth (5.x/LE), NFC, 5G/LTE
- **Enterprise Protocols:** LDAP, Kerberos, SNMP, NTP, SIP, RADIUS
- **Data Formats:** JSON, XML, Protocol Buffers, CBOR, MessagePack

Understanding protocol specifications, implementation patterns, security considerations, and performance characteristics is crucial for network engineers, software developers, system integrators, and IoT architects working across telecommunications, industrial automation, enterprise IT, and consumer electronics.

**背景：** 协议标准是现代通信系统的基本构建块，使不同设备、系统和网络之间的互操作成为可能。从支撑全球连接的互联网协议到驱动自动化和智能系统的专业工业和物联网协议，理解这些标准对于从事网络、软件开发、系统集成或物联网工作的任何人都至关重要。

协议标准解决关键挑战：
- **互操作性：** 使来自不同供应商的异构系统能够通信
- **可靠性：** 定义错误检测、纠正和恢复机制
- **安全性：** 建立加密、认证和授权框架
- **可扩展性：** 支持从小型传感器网络到全球互联网基础设施的系统
- **演进：** 在引入新功能的同时保持向后兼容性

协议领域跨越多个域：
- **互联网协议：** TCP/IP套件、HTTP/HTTPS、WebSocket、QUIC、DNS、DHCP、SMTP、FTP
- **工业协议：** Modbus、PROFIBUS、PROFINET、EtherCAT、OPC UA、CAN总线
- **物联网协议：** MQTT、CoAP、AMQP、LoRaWAN、Zigbee、Thread
- **无线标准：** Wi-Fi（802.11ax/6）、蓝牙（5.x/LE）、NFC、5G/LTE
- **企业协议：** LDAP、Kerberos、SNMP、NTP、SIP、RADIUS
- **数据格式：** JSON、XML、Protocol Buffers、CBOR、MessagePack

理解协议规范、实现模式、安全考虑和性能特征对于从事电信、工业自动化、企业IT和消费电子领域的网络工程师、软件开发人员、系统集成商和物联网架构师至关重要。

## I - Intent (意图)
**Goal:** Create a comprehensive, authoritative, and practical technical documentation that thoroughly covers common protocol standards across networking, industrial, IoT, and wireless domains. The documentation should serve as both a learning resource for protocol fundamentals and a reference guide for protocol implementation and troubleshooting.

**Objectives:**
1. Explain the OSI and TCP/IP reference models
2. Cover core Internet protocols: TCP, UDP, IP, HTTP/HTTPS, DNS, DHCP
3. Detail application layer protocols: SMTP, FTP, SSH, WebSocket
4. Introduce industrial protocols: Modbus, PROFINET, OPC UA, CAN bus
5. Describe IoT protocols: MQTT, CoAP, AMQP, LoRaWAN
6. Cover wireless standards: Wi-Fi, Bluetooth, Zigbee, 5G
7. Explain enterprise protocols: LDAP, SNMP, NTP, Kerberos
8. Detail security protocols: TLS/SSL, IPsec, OAuth, JWT
9. Provide protocol packet structure analysis and examples
10. Compare protocols for different use cases and requirements

**目标：** 创建一份全面、权威且实用的技术文档，深入覆盖跨网络、工业、物联网和无线领域的常用协议标准。该文档既可作为协议基础的学习资源，也可作为协议实现和故障排除的参考指南。

**具体目标：**
1. 解释OSI和TCP/IP参考模型
2. 涵盖核心互联网协议：TCP、UDP、IP、HTTP/HTTPS、DNS、DHCP
3. 详细介绍应用层协议：SMTP、FTP、SSH、WebSocket
4. 介绍工业协议：Modbus、PROFINET、OPC UA、CAN总线
5. 描述物联网协议：MQTT、CoAP、AMQP、LoRaWAN
6. 涵盖无线标准：Wi-Fi、蓝牙、Zigbee、5G
7. 解释企业协议：LDAP、SNMP、NTP、Kerberos
8. 详细介绍安全协议：TLS/SSL、IPsec、OAuth、JWT
9. 提供协议数据包结构分析和示例
10. 比较不同用例和需求的协议

## S - Statement (详细说明)
**Detailed Requirements:**

### Content Scope:
**Part 1 - Protocol Fundamentals:**
- OSI 7-layer model: Physical, Data Link, Network, Transport, Session, Presentation, Application
- TCP/IP 4-layer model: Network Access, Internet, Transport, Application
- Protocol design principles: encapsulation, layering, addressing, routing
- Protocol data units: frames, packets, segments, messages
- Error detection and correction: checksums, CRC, parity
- Flow control and congestion control mechanisms

**Part 2 - Internet Core Protocols:**
- **IP (Internet Protocol):** IPv4 vs IPv6, addressing, subnetting, CIDR, NAT
- **TCP (Transmission Control Protocol):** Three-way handshake, flow control, congestion control, connection termination
- **UDP (User Datagram Protocol):** Connectionless communication, use cases
- **ICMP (Internet Control Message Protocol):** Ping, traceroute, error reporting
- **ARP/NDP:** Address resolution, neighbor discovery

**Part 3 - Application Layer Protocols:**
- **HTTP/HTTPS:** Request/response model, methods (GET, POST, PUT, DELETE), status codes, headers, HTTP/2, HTTP/3 (QUIC)
- **DNS:** Domain name resolution, record types (A, AAAA, CNAME, MX, TXT), recursive vs iterative queries, DNSSEC
- **DHCP:** Dynamic IP allocation, DORA process (Discover, Offer, Request, Acknowledge)
- **SMTP/POP3/IMAP:** Email protocols, message format, authentication
- **FTP/SFTP:** File transfer, active vs passive mode
- **SSH:** Secure shell, key exchange, authentication
- **WebSocket:** Full-duplex communication over TCP

**Part 4 - Industrial Protocols:**
- **Modbus:** RTU vs TCP, function codes, register addressing
- **PROFINET:** Real-time Ethernet, device configuration, cyclic vs acyclic communication
- **OPC UA:** Client-server architecture, information modeling, security
- **CAN bus:** Arbitration, message format, automotive applications
- **EtherCAT:** Distributed clocks, topology, performance
- **PROFIBUS:** DP vs PA variants, master-slave communication

**Part 5 - IoT Protocols:**
- **MQTT:** Publish-subscribe model, QoS levels (0, 1, 2), topics, retained messages, last will
- **CoAP:** RESTful protocol for constrained devices, request/response model, observe pattern
- **AMQP:** Message queuing, exchanges, bindings, routing
- **LoRaWAN:** Long-range, low-power, device classes (A, B, C), network architecture
- **Zigbee:** Mesh networking, device types (coordinator, router, end device), profiles
- **Thread:** IPv6-based mesh, border router, commissioning

**Part 6 - Wireless Standards:**
- **Wi-Fi:** 802.11 standards (a/b/g/n/ac/ax), channel bonding, MIMO, WPA2/WPA3 security
- **Bluetooth:** Classic vs Low Energy (LE), GATT profiles, pairing, advertising
- **NFC:** Near-field communication, card emulation, peer-to-peer, reader/writer modes
- **5G/LTE:** Network slicing, beamforming, millimeter wave, NR (New Radio)
- **LoRa:** Modulation, spreading factor, adaptive data rate

**Part 7 - Enterprise Protocols:**
- **LDAP:** Directory services, DN/RDN structure, search filters, schema
- **SNMP:** Network management, MIB (Management Information Base), traps, versions (v1, v2c, v3)
- **NTP:** Time synchronization, stratum levels, accuracy
- **Kerberos:** Ticket-granting service, authentication flow, realm
- **RADIUS:** AAA (Authentication, Authorization, Accounting), NAS integration
- **SIP:** VoIP signaling, call setup, RTP/RTCP

**Part 8 - Security Protocols:**
- **TLS/SSL:** Handshake, cipher suites, certificates, TLS 1.2 vs 1.3
- **IPsec:** ESP vs AH, tunnel vs transport mode, IKE (Internet Key Exchange)
- **OAuth 2.0:** Authorization flows, access tokens, refresh tokens
- **JWT (JSON Web Token):** Structure, signing, claims
- **SAML:** Single sign-on, assertions, identity provider

**Part 9 - Data Serialization Formats:**
- **JSON:** Text-based, human-readable, schema validation
- **XML:** Document structure, namespaces, XSD schemas
- **Protocol Buffers:** Binary format, schema definition, code generation
- **CBOR:** Concise binary object representation, IoT applications
- **MessagePack:** Efficient serialization, cross-language support

**Part 10 - Protocol Analysis and Troubleshooting:**
- Wireshark packet capture and analysis
- Protocol conformance testing
- Performance metrics: latency, throughput, jitter, packet loss
- Common protocol issues and debugging strategies
- Interoperability testing

### Technical Depth:
- Protocol packet structure diagrams with field explanations
- Sequence diagrams for protocol handshakes and message flows
- Code examples for protocol implementation (Python, C, JavaScript)
- Configuration snippets for protocol setup
- Wireshark capture examples and filter syntax
- Performance benchmarks and comparison tables
- Security considerations and best practices

### Presentation Style:
- Bilingual format: **English first, followed by Chinese translation**
- Clear section hierarchy with descriptive headings
- Technical terminology with both English and Chinese terms
- Practical examples and real-world use cases
- Comparison tables for protocol selection
- Best practices and common pitfalls

**详细要求：**

### 内容范围：
**第一部分 - 协议基础：**
- OSI 7层模型：物理层、数据链路层、网络层、传输层、会话层、表示层、应用层
- TCP/IP 4层模型：网络接入层、互联网层、传输层、应用层
- 协议设计原则：封装、分层、寻址、路由
- 协议数据单元：帧、数据包、段、消息
- 错误检测和纠正：校验和、CRC、奇偶校验
- 流控制和拥塞控制机制

**第二部分 - 互联网核心协议：**
- **IP（互联网协议）：** IPv4 vs IPv6、寻址、子网划分、CIDR、NAT
- **TCP（传输控制协议）：** 三次握手、流控制、拥塞控制、连接终止
- **UDP（用户数据报协议）：** 无连接通信、用例
- **ICMP（互联网控制消息协议）：** Ping、traceroute、错误报告
- **ARP/NDP：** 地址解析、邻居发现

**第三部分 - 应用层协议：**
- **HTTP/HTTPS：** 请求/响应模型、方法（GET、POST、PUT、DELETE）、状态码、头部、HTTP/2、HTTP/3（QUIC）
- **DNS：** 域名解析、记录类型（A、AAAA、CNAME、MX、TXT）、递归vs迭代查询、DNSSEC
- **DHCP：** 动态IP分配、DORA过程（发现、提供、请求、确认）
- **SMTP/POP3/IMAP：** 电子邮件协议、消息格式、认证
- **FTP/SFTP：** 文件传输、主动vs被动模式
- **SSH：** 安全外壳、密钥交换、认证
- **WebSocket：** TCP上的全双工通信

**第四部分 - 工业协议：**
- **Modbus：** RTU vs TCP、功能码、寄存器寻址
- **PROFINET：** 实时以太网、设备配置、循环vs非循环通信
- **OPC UA：** 客户端-服务器架构、信息建模、安全性
- **CAN总线：** 仲裁、消息格式、汽车应用
- **EtherCAT：** 分布式时钟、拓扑、性能
- **PROFIBUS：** DP vs PA变体、主从通信

**第五部分 - 物联网协议：**
- **MQTT：** 发布-订阅模型、QoS级别（0、1、2）、主题、保留消息、遗嘱
- **CoAP：** 受限设备的RESTful协议、请求/响应模型、观察模式
- **AMQP：** 消息队列、交换机、绑定、路由
- **LoRaWAN：** 长距离、低功耗、设备类别（A、B、C）、网络架构
- **Zigbee：** 网状网络、设备类型（协调器、路由器、终端设备）、配置文件
- **Thread：** 基于IPv6的网状、边界路由器、调试

**第六部分 - 无线标准：**
- **Wi-Fi：** 802.11标准（a/b/g/n/ac/ax）、信道绑定、MIMO、WPA2/WPA3安全
- **蓝牙：** 经典vs低功耗（LE）、GATT配置文件、配对、广播
- **NFC：** 近场通信、卡模拟、点对点、读写器模式
- **5G/LTE：** 网络切片、波束成形、毫米波、NR（新无线电）
- **LoRa：** 调制、扩频因子、自适应数据速率

**第七部分 - 企业协议：**
- **LDAP：** 目录服务、DN/RDN结构、搜索过滤器、模式
- **SNMP：** 网络管理、MIB（管理信息库）、陷阱、版本（v1、v2c、v3）
- **NTP：** 时间同步、层级、精度
- **Kerberos：** 票据授予服务、认证流程、域
- **RADIUS：** AAA（认证、授权、计费）、NAS集成
- **SIP：** VoIP信令、呼叫建立、RTP/RTCP

**第八部分 - 安全协议：**
- **TLS/SSL：** 握手、密码套件、证书、TLS 1.2 vs 1.3
- **IPsec：** ESP vs AH、隧道vs传输模式、IKE（互联网密钥交换）
- **OAuth 2.0：** 授权流程、访问令牌、刷新令牌
- **JWT（JSON Web Token）：** 结构、签名、声明
- **SAML：** 单点登录、断言、身份提供者

**第九部分 - 数据序列化格式：**
- **JSON：** 基于文本、人类可读、模式验证
- **XML：** 文档结构、命名空间、XSD模式
- **Protocol Buffers：** 二进制格式、模式定义、代码生成
- **CBOR：** 简洁二进制对象表示、物联网应用
- **MessagePack：** 高效序列化、跨语言支持

**第十部分 - 协议分析和故障排除：**
- Wireshark数据包捕获和分析
- 协议一致性测试
- 性能指标：延迟、吞吐量、抖动、丢包
- 常见协议问题和调试策略
- 互操作性测试

### 技术深度：
- 带字段解释的协议数据包结构图
- 协议握手和消息流的序列图
- 协议实现的代码示例（Python、C、JavaScript）
- 协议设置的配置片段
- Wireshark捕获示例和过滤器语法
- 性能基准和比较表
- 安全考虑和最佳实践

### 呈现风格：
- 双语格式：**英文在前，中文翻译在后**
- 清晰的章节层次和描述性标题
- 技术术语采用中英文对照
- 实际示例和真实用例
- 协议选择的比较表格
- 最佳实践和常见陷阱

## P - Personality (个性风格)
**Writing Style:**
- **Technical and Precise:** Use accurate protocol terminology and specifications
- **Structured and Systematic:** Organize content by protocol layers and domains
- **Practical and Applied:** Focus on real-world implementation and use cases
- **Comparative and Analytical:** Compare protocols to guide selection decisions
- **Standards-Based:** Reference official RFCs and specifications
- **Accessible yet Detailed:** Balance comprehensiveness with clarity for intermediate learners

**Tone:**
- Professional and authoritative
- Protocol-focused with practical implementation guidance
- Detailed in packet structure and message flow explanations
- Include troubleshooting tips and debugging strategies
- Emphasize interoperability and standards compliance

**写作风格：**
- **技术和精确：** 使用准确的协议术语和规范
- **结构化和系统化：** 按协议层和域组织内容
- **实用和应用导向：** 关注实际实现和用例
- **比较和分析性：** 比较协议以指导选择决策
- **基于标准：** 引用官方RFC和规范
- **易懂但详细：** 平衡全面性和中级学习者的清晰度

**语气：**
- 专业和权威
- 协议聚焦，提供实用实现指导
- 数据包结构和消息流解释详细
- 包含故障排除提示和调试策略
- 强调互操作性和标准合规性

## E - Experiment (预期输出)
**Expected Output Format:**

```markdown
# Common Protocol Standards - Technical Documentation
# 常用的协议标准 - 技术文档

## 1. Protocol Fundamentals / 协议基础
### 1.1 OSI and TCP/IP Models / OSI和TCP/IP模型
[English content...]
[中文内容...]

### 1.2 Protocol Design Principles / 协议设计原则
[English content...]
[中文内容...]

## 2. Internet Core Protocols / 互联网核心协议
### 2.1 IP, TCP, UDP / IP、TCP、UDP
[Detailed sections with packet structures...]

## 3. Application Layer Protocols / 应用层协议
[Detailed sections with bilingual content...]

## 4. Industrial Protocols / 工业协议
[Detailed sections with bilingual content...]

## 5. IoT Protocols / 物联网协议
[Detailed sections with bilingual content...]

## 6. Wireless Standards / 无线标准
[Detailed sections with bilingual content...]

## 7. Enterprise Protocols / 企业协议
[Detailed sections with bilingual content...]

## 8. Security Protocols / 安全协议
[Detailed sections with bilingual content...]

## 9. Data Serialization Formats / 数据序列化格式
[Detailed sections with bilingual content...]

## 10. Protocol Analysis and Troubleshooting / 协议分析和故障排除
[Detailed sections with bilingual content...]
```

**Execution Instructions:**
1. Start with fundamental networking models (OSI, TCP/IP)
2. Progress through protocol layers from low to high
3. Maintain consistent bilingual format throughout (English → Chinese)
4. Include packet structure diagrams for major protocols
5. Provide code examples for protocol implementation
6. Compare protocols with tables highlighting strengths/weaknesses
7. End with practical troubleshooting and analysis techniques
8. Include Wireshark examples for key protocols

**执行说明：**
1. 从基本网络模型（OSI、TCP/IP）开始
2. 从低到高逐步深入协议层
3. 全文保持一致的双语格式（英文→中文）
4. 为主要协议包含数据包结构图
5. 提供协议实现的代码示例
6. 用表格比较协议，突出优缺点
7. 以实用的故障排除和分析技术结束
8. 为关键协议包含Wireshark示例

---

**This CRISPE framework provides the foundation for creating comprehensive technical documentation on common protocol standards, ensuring coverage of Internet, industrial, IoT, wireless, and enterprise protocols with clear bilingual presentation and practical implementation guidance.**

**此CRISPE框架为创建关于常用协议标准的全面技术文档提供了基础，确保涵盖互联网、工业、物联网、无线和企业协议，并提供清晰的双语呈现和实用的实施指导。**
