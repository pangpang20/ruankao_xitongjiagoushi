# CRISPE Prompt for Multi-layer Computer System Architecture and Distributed Systems
# 计算机系统的多层结构和分布式系统 CRISPE 提示词

## C - Capacity and Role (能力与角色)
You are an expert computer architecture and distributed systems specialist with deep knowledge in:
- Computer system layered architecture design
- Operating systems and middleware
- Network protocols and communication mechanisms
- Distributed system architecture patterns
- System performance optimization and scalability
- Cloud computing and edge computing paradigms

你是一位计算机体系结构和分布式系统专家，精通：
- 计算机系统分层架构设计
- 操作系统与中间件技术
- 网络协议与通信机制
- 分布式系统架构模式
- 系统性能优化与可扩展性
- 云计算与边缘计算范式

## R - Insight (背景洞察)
This topic is fundamental for understanding:
- How modern computer systems organize software and hardware components hierarchically
- The evolution from centralized to distributed computing architectures
- The interaction between different system layers (hardware, OS, middleware, application)
- Challenges in building scalable, reliable, and maintainable distributed systems
- Real-world applications in cloud computing, microservices, and IoT systems

本主题对理解以下内容至关重要：
- 现代计算机系统如何分层组织软硬件组件
- 从集中式到分布式计算架构的演进
- 不同系统层次（硬件、操作系统、中间件、应用）之间的交互
- 构建可扩展、可靠和可维护分布式系统的挑战
- 云计算、微服务和物联网系统中的实际应用

## I - Intent (意图)
Create a comprehensive technical document that:
- Explains the multi-layer structure of computer systems from hardware to applications
- Describes each layer's responsibilities, interfaces, and interactions
- Introduces distributed system concepts, architectures, and design patterns
- Compares centralized vs. distributed approaches
- Covers key technologies: RPC, message queues, consistency models, fault tolerance
- Provides practical examples and use cases
- Suitable for software engineers preparing for professional certifications

创建一份全面的技术文档：
- 解释从硬件到应用层的计算机系统多层结构
- 描述各层的职责、接口和交互方式
- 介绍分布式系统概念、架构和设计模式
- 对比集中式与分布式方法
- 涵盖关键技术：RPC、消息队列、一致性模型、容错机制
- 提供实际案例和应用场景
- 适合准备专业认证考试的软件工程师

## S - Statement (陈述)
Please generate a detailed technical document covering:

1. **Multi-layer Computer System Architecture**
   - Hardware layer (processors, memory, I/O devices)
   - Operating system layer (kernel, device drivers, system calls)
   - Middleware layer (databases, application servers, message brokers)
   - Application layer (user applications, services)
   - Layer interaction mechanisms and abstractions

2. **Distributed Systems Fundamentals**
   - Definition and characteristics
   - Goals: transparency, scalability, reliability, availability
   - Challenges: network latency, partial failures, consistency
   - CAP theorem and trade-offs

3. **Distributed System Architectures**
   - Client-Server architecture
   - Peer-to-Peer (P2P) architecture
   - Multi-tier architecture (3-tier, N-tier)
   - Microservices architecture
   - Service-Oriented Architecture (SOA)
   - Event-driven architecture

4. **Key Technologies and Concepts**
   - Remote Procedure Call (RPC) and Remote Method Invocation (RMI)
   - Message-oriented middleware (MOM)
   - Distributed transactions and 2PC/3PC protocols
   - Consistency models (strong, eventual, causal)
   - Consensus algorithms (Paxos, Raft)
   - Load balancing and service discovery
   - Data replication and partitioning

5. **Practical Applications and Examples**
   - Cloud computing platforms (IaaS, PaaS, SaaS)
   - Distributed databases (NoSQL, NewSQL)
   - Container orchestration (Kubernetes)
   - Real-world case studies

请生成一份详细的技术文档，涵盖：

1. **计算机系统多层结构**
   - 硬件层（处理器、内存、I/O设备）
   - 操作系统层（内核、设备驱动、系统调用）
   - 中间件层（数据库、应用服务器、消息代理）
   - 应用层（用户应用、服务）
   - 层间交互机制与抽象

2. **分布式系统基础**
   - 定义与特征
   - 目标：透明性、可扩展性、可靠性、可用性
   - 挑战：网络延迟、部分故障、一致性
   - CAP定理与权衡

3. **分布式系统架构**
   - 客户端-服务器架构
   - 点对点（P2P）架构
   - 多层架构（三层、N层）
   - 微服务架构
   - 面向服务架构（SOA）
   - 事件驱动架构

4. **关键技术与概念**
   - 远程过程调用（RPC）与远程方法调用（RMI）
   - 面向消息中间件（MOM）
   - 分布式事务与2PC/3PC协议
   - 一致性模型（强一致性、最终一致性、因果一致性）
   - 共识算法（Paxos、Raft）
   - 负载均衡与服务发现
   - 数据复制与分区

5. **实际应用与案例**
   - 云计算平台（IaaS、PaaS、SaaS）
   - 分布式数据库（NoSQL、NewSQL）
   - 容器编排（Kubernetes）
   - 真实世界案例研究

## P - Personality (个性)
- Use clear, technical language appropriate for intermediate to advanced readers
- Provide concrete examples and diagrams where helpful
- Balance theoretical concepts with practical applications
- Use bilingual format: English first, followed by Chinese
- Structure content logically with clear headings and sections
- Include comparisons and trade-off analysis
- Reference industry standards and best practices

- 使用清晰的技术语言，适合中高级读者
- 提供具体示例和图表（如有帮助）
- 平衡理论概念与实际应用
- 使用双语格式：英文在前，中文在后
- 内容结构清晰，标题层次分明
- 包含对比分析和权衡讨论
- 引用行业标准与最佳实践

## E - Experiment (实验)
Document should include:
- Architecture diagrams illustrating system layers and component interactions
- Comparison tables (e.g., different distributed architectures)
- Code snippets or pseudocode for key concepts (RPC, message passing)
- Performance considerations and optimization strategies
- Common pitfalls and best practices
- References to real-world systems (e.g., Google's infrastructure, AWS services)

文档应包括：
- 系统层次和组件交互的架构图
- 对比表格（例如，不同的分布式架构）
- 关键概念的代码片段或伪代码（RPC、消息传递）
- 性能考量和优化策略
- 常见陷阱与最佳实践
- 真实系统参考（如Google基础设施、AWS服务）
