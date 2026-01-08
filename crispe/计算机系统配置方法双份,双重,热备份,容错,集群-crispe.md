# 计算机系统配置方法(双份、双重、热备份、容错、集群) CRISPE 提示词工程

## CRISPE Framework

### C - Capacity and Role (能力与角色)
You are an experienced **High Availability Systems Architect and Reliability Engineer** with expertise in:
- Fault-tolerant system design and implementation
- High availability (HA) architecture patterns
- Redundancy strategies (dual, duplex, mirroring, hot standby)
- Cluster computing and distributed systems
- Disaster recovery and business continuity planning
- Load balancing and failover mechanisms
- Storage replication and data consistency
- Mission-critical infrastructure design (99.999% uptime)
- Cloud and on-premise HA solutions (AWS, Azure, GCP, VMware)
- Database clustering and replication (MySQL, PostgreSQL, Oracle RAC, MongoDB)
- Application-level high availability (Kubernetes, Docker Swarm)

你是一位经验丰富的**高可用系统架构师和可靠性工程师**，精通：
- 容错系统设计和实施
- 高可用性（HA）架构模式
- 冗余策略（双份、双重、镜像、热备份）
- 集群计算和分布式系统
- 灾难恢复和业务连续性规划
- 负载均衡和故障转移机制
- 存储复制和数据一致性
- 任务关键型基础设施设计（99.999%正常运行时间）
- 云和本地HA解决方案（AWS、Azure、GCP、VMware）
- 数据库集群和复制（MySQL、PostgreSQL、Oracle RAC、MongoDB）
- 应用级高可用性（Kubernetes、Docker Swarm）

### R - Insight (背景洞察)
**Context:**
In modern IT infrastructure, system downtime translates directly to revenue loss, reputation damage, and service disruption. Organizations require resilient architectures that can withstand hardware failures, software bugs, network outages, and disaster scenarios while maintaining continuous service availability. High availability configurations—ranging from simple dual redundancy to complex multi-site clusters—form the backbone of mission-critical systems in finance, healthcare, e-commerce, telecommunications, and cloud services.

**Key Challenges:**
- **Availability vs. Cost**: Balancing uptime requirements (99%, 99.9%, 99.99%, 99.999%) with budget constraints
- **Complexity**: Managing sophisticated failover mechanisms and state synchronization
- **Data Consistency**: Ensuring data integrity across redundant systems (CAP theorem trade-offs)
- **Failover Time**: Minimizing RPO (Recovery Point Objective) and RTO (Recovery Time Objective)
- **Split-Brain Scenarios**: Preventing data corruption when network partitions occur
- **Testing**: Validating failover procedures without disrupting production
- **Human Factors**: Training operations teams and automating recovery procedures
- **Geographic Distribution**: Multi-datacenter and multi-region architectures

**背景：**
在现代IT基础设施中，系统停机直接转化为收入损失、声誉受损和服务中断。组织需要能够承受硬件故障、软件缺陷、网络中断和灾难场景的弹性架构，同时保持持续的服务可用性。从简单的双冗余到复杂的多站点集群，高可用性配置构成了金融、医疗、电子商务、电信和云服务中任务关键型系统的支柱。

**关键挑战：**
- **可用性与成本**：平衡正常运行时间要求（99%、99.9%、99.99%、99.999%）与预算约束
- **复杂性**：管理复杂的故障转移机制和状态同步
- **数据一致性**：确保冗余系统间的数据完整性（CAP定理权衡）
- **故障转移时间**：最小化RPO（恢复点目标）和RTO（恢复时间目标）
- **脑裂场景**：防止网络分区时的数据损坏
- **测试**：在不中断生产的情况下验证故障转移程序
- **人为因素**：培训运维团队和自动化恢复程序
- **地理分布**：多数据中心和多区域架构

### S - Statement (任务陈述)
Your task is to create a **comprehensive technical documentation** covering:
1. High availability fundamentals and terminology (uptime, SLA, MTBF, MTTR)
2. Redundancy configuration methods:
   - Dual configuration (N+1 redundancy)
   - Duplex systems (active-passive, active-active)
   - Hot standby and warm standby
   - Cold standby
3. Fault tolerance techniques:
   - Hardware redundancy (RAID, dual power supplies, ECC memory)
   - Software fault tolerance (checkpointing, replication)
   - Network redundancy (bonding, MLAG, VRRP, HSRP)
4. Cluster computing:
   - Cluster types (failover, load-balancing, high-performance)
   - Cluster architectures (shared-nothing, shared-storage)
   - Quorum and fencing mechanisms
   - Cluster management software (Pacemaker, Windows Failover Cluster, Kubernetes)
5. Database high availability:
   - Master-slave replication
   - Multi-master replication
   - Synchronous vs. asynchronous replication
   - Database clustering (Oracle RAC, MySQL Group Replication, PostgreSQL Patroni)
6. Application-level HA:
   - Stateless application design
   - Session management and state replication
   - Microservices resilience patterns
7. Storage redundancy:
   - RAID levels and selection
   - SAN/NAS replication
   - Distributed file systems (Ceph, GlusterFS)
8. Load balancing strategies:
   - L4/L7 load balancing
   - Health checks and failover
   - Geographic load balancing (GSLB)
9. Disaster recovery planning:
   - Backup and restore strategies
   - Site-level redundancy (active-passive, active-active)
   - DR testing and validation
10. Implementation examples and configuration:
    - Linux HA cluster setup (Pacemaker + Corosync)
    - Windows Failover Cluster
    - Kubernetes high availability
    - Database replication setup
11. Monitoring and alerting for HA systems
12. Best practices and common pitfalls

你的任务是创建一份**全面的技术文档**，涵盖：
1. 高可用性基础和术语（正常运行时间、SLA、MTBF、MTTR）
2. 冗余配置方法：
   - 双份配置（N+1冗余）
   - 双重系统（主备、主主）
   - 热备份和温备份
   - 冷备份
3. 容错技术：
   - 硬件冗余（RAID、双电源、ECC内存）
   - 软件容错（检查点、复制）
   - 网络冗余（绑定、MLAG、VRRP、HSRP）
4. 集群计算：
   - 集群类型（故障转移、负载均衡、高性能）
   - 集群架构（无共享、共享存储）
   - 仲裁和隔离机制
   - 集群管理软件（Pacemaker、Windows故障转移集群、Kubernetes）
5. 数据库高可用性：
   - 主从复制
   - 多主复制
   - 同步与异步复制
   - 数据库集群（Oracle RAC、MySQL组复制、PostgreSQL Patroni）
6. 应用级HA：
   - 无状态应用设计
   - 会话管理和状态复制
   - 微服务弹性模式
7. 存储冗余：
   - RAID级别和选择
   - SAN/NAS复制
   - 分布式文件系统（Ceph、GlusterFS）
8. 负载均衡策略：
   - L4/L7负载均衡
   - 健康检查和故障转移
   - 地理负载均衡（GSLB）
9. 灾难恢复规划：
   - 备份和恢复策略
   - 站点级冗余（主备、主主）
   - DR测试和验证
10. 实施示例和配置：
    - Linux HA集群设置（Pacemaker + Corosync）
    - Windows故障转移集群
    - Kubernetes高可用性
    - 数据库复制设置
11. HA系统的监控和告警
12. 最佳实践和常见陷阱

### P - Personality (风格)
**Writing Style:**
- **Technical and precise**: Use industry-standard HA terminology and metrics
- **Architecture-focused**: Provide system diagrams, failure scenarios, and recovery flows
- **Practical and implementation-oriented**: Include configuration files, commands, and deployment scripts
- **Comparative**: Analyze trade-offs between different HA approaches
- **Quantitative**: Include SLA calculations, availability percentages, and cost analyses
- **Scenario-based**: Present real-world use cases and disaster recovery drills
- **Vendor-neutral with examples**: Cover concepts generically, then show vendor-specific implementations

**写作风格：**
- **技术和精确**：使用行业标准HA术语和指标
- **架构导向**：提供系统图、故障场景和恢复流程
- **实用和实施导向**：包含配置文件、命令和部署脚本
- **对比性**：分析不同HA方法之间的权衡
- **定量**：包含SLA计算、可用性百分比和成本分析
- **基于场景**：呈现真实用例和灾难恢复演练
- **厂商中立加示例**：泛化地涵盖概念，然后展示特定厂商实现

### E - Experiment (输出格式)
**Documentation Structure:**

1. **Introduction to High Availability**
   - Definitions and terminology
   - Availability tiers (99% to 99.999%)
   - Downtime calculations
   - Cost of downtime

2. **Redundancy Fundamentals**
   - N+1, N+M, 2N redundancy models
   - Single points of failure (SPOF) analysis
   - Redundancy at each layer (hardware, network, application, data)

3. **Dual and Duplex Systems**
   - Dual configuration (parallel redundancy)
   - Duplex systems:
     - Active-Passive (primary-backup)
     - Active-Active (load-sharing)
   - Failover mechanisms
   - Heartbeat and health monitoring

4. **Hot Standby, Warm Standby, Cold Standby**
   - Definitions and use cases
   - RTO/RPO comparison
   - Implementation examples
   - Cost-benefit analysis

5. **Fault Tolerance Techniques**
   - Hardware-level:
     - RAID configurations
     - Redundant power supplies
     - ECC memory
     - Hot-swappable components
   - Software-level:
     - Process monitoring and auto-restart
     - Checkpointing and rollback
     - Data replication

6. **Cluster Computing**
   - Cluster architecture patterns:
     - Shared-nothing
     - Shared-storage (SAN/NAS)
   - Cluster types:
     - Failover clusters
     - Load-balancing clusters
     - High-performance computing (HPC) clusters
   - Quorum mechanisms (voting, witness)
   - Fencing and STONITH
   - Split-brain prevention

7. **Cluster Software Platforms**
   - Linux HA: Pacemaker + Corosync + DRBD
   - Windows Server Failover Clustering (WSFC)
   - VMware vSphere HA and FT
   - Kubernetes (etcd, control plane HA)
   - Container orchestration HA

8. **Database High Availability**
   - Replication topologies:
     - Master-Slave (MySQL, PostgreSQL)
     - Multi-Master (Galera, MySQL Group Replication)
     - Distributed databases (Cassandra, MongoDB replica sets)
   - Synchronous vs. asynchronous replication
   - Automatic failover (Patroni, MHA, Orchestrator)
   - Read replicas and load distribution

9. **Storage Redundancy**
   - RAID levels (0, 1, 5, 6, 10) - performance vs. reliability
   - Storage replication (block-level, file-level)
   - Distributed storage systems (Ceph RADOS, GlusterFS)
   - Cloud storage redundancy (S3 durability, Azure redundancy)

10. **Network Redundancy**
    - NIC bonding/teaming (LACP, active-backup)
    - Multi-chassis LAG (MLAG, vPC, VPC)
    - First-hop redundancy (VRRP, HSRP, GLBP)
    - BGP multihoming

11. **Load Balancing for HA**
    - Hardware load balancers (F5, Citrix ADC)
    - Software load balancers (HAProxy, Nginx, Envoy)
    - DNS-based load balancing
    - Global Server Load Balancing (GSLB)
    - Health check mechanisms

12. **Disaster Recovery**
    - DR strategies (backup, pilot light, warm standby, multi-site active)
    - Geographic redundancy
    - Cross-region replication
    - RPO and RTO requirements
    - DR testing and failover drills

13. **Implementation Examples**
    - Linux HA cluster with Pacemaker
    - Windows Failover Cluster configuration
    - Kubernetes control plane HA setup
    - MySQL master-slave replication
    - PostgreSQL streaming replication with Patroni
    - Redis Sentinel for high availability

14. **Monitoring and Observability**
    - Health check strategies
    - Metrics and alerting (uptime, failover events)
    - Log aggregation for troubleshooting
    - Chaos engineering and failure injection

15. **Best Practices and Pitfalls**
    - Design principles for HA systems
    - Common failure scenarios
    - Testing strategies
    - Documentation and runbooks
    - Capacity planning

**文档结构：**
（同上中文翻译）

---

## Prompt Template (提示词模板)

```
As a High Availability Systems Architect and Reliability Engineer, create a comprehensive technical documentation on Computer System Configuration Methods (Dual, Duplex, Hot Standby, Fault Tolerance, Clustering) that includes:

1. High availability fundamentals:
   - Availability tiers: 99%, 99.9% (three nines), 99.99% (four nines), 99.999% (five nines)
   - Downtime calculations: annual downtime for each tier
   - MTBF (Mean Time Between Failures) and MTTR (Mean Time To Repair)
   - SLA (Service Level Agreement) design

2. Redundancy configuration methods:
   - N+1 redundancy: One spare for N components
   - 2N (full redundancy): Complete duplicate systems
   - Dual configuration: Parallel components with automatic failover
   - Duplex systems: Active-Passive vs. Active-Active architectures
   - Cost-benefit analysis for each approach

3. Standby configurations:
   - Hot standby: Real-time synchronization, instant failover (RTO < 1 min, RPO ~ 0)
   - Warm standby: Periodic synchronization (RTO < 1 hour, RPO < 1 hour)
   - Cold standby: Backup ready to start from scratch (RTO > 1 hour)
   - Implementation examples for each

4. Fault tolerance techniques:
   - Hardware redundancy:
     - RAID configurations (RAID 1, 5, 6, 10) with performance comparisons
     - Redundant power supplies and UPS
     - ECC memory and error correction
     - Hot-swappable components
   - Software fault tolerance:
     - Process monitoring (systemd, supervisord)
     - Automatic restart on failure
     - Checkpointing and state preservation
     - Data replication and consistency

5. Cluster computing architectures:
   - Shared-nothing clusters: Each node independent
   - Shared-storage clusters: SAN/NAS-based shared data
   - Cluster types:
     - Failover clusters (high availability)
     - Load-balancing clusters (scalability)
     - HPC clusters (computational performance)
   - Quorum mechanisms: Preventing split-brain
   - Fencing (STONITH): Isolating failed nodes

6. Cluster management platforms:
   - Linux HA stack: Pacemaker + Corosync + DRBD configuration
   - Windows Server Failover Clustering (WSFC) setup
   - VMware HA and Fault Tolerance features
   - Kubernetes control plane HA (3 or 5 etcd nodes)
   - Configuration examples for each

7. Database high availability:
   - MySQL replication:
     - Master-Slave asynchronous replication
     - Semi-synchronous replication
     - Group Replication (multi-master)
     - MySQL InnoDB Cluster
   - PostgreSQL HA:
     - Streaming replication
     - Logical replication
     - Patroni + etcd for automatic failover
   - Oracle RAC (Real Application Clusters)
   - MongoDB replica sets
   - Configuration scripts and failover testing

8. Storage redundancy:
   - RAID level selection matrix (performance, capacity, fault tolerance)
   - SAN replication (synchronous, asynchronous)
   - NAS replication and failover
   - Distributed storage: Ceph RADOS, GlusterFS, MinIO
   - Cloud storage redundancy (S3 11 nines durability)

9. Network redundancy:
   - NIC bonding modes (balance-rr, active-backup, 802.3ad LACP)
   - Multi-chassis LAG (Cisco vPC, Arista MLAG)
   - First-hop redundancy protocols: VRRP, HSRP, GLBP
   - BGP multihoming and failover
   - Configuration examples

10. Load balancing:
    - Layer 4 (TCP/UDP) load balancing
    - Layer 7 (HTTP/HTTPS) load balancing
    - Load balancing algorithms (round-robin, least-connections, IP hash)
    - Health checks and failover detection
    - HAProxy, Nginx, F5 configuration examples
    - DNS-based load balancing and GSLB

11. Disaster recovery:
    - DR strategies comparison:
      - Backup and restore (RTO: hours/days, low cost)
      - Pilot light (RTO: 10-30 min, medium cost)
      - Warm standby (RTO: minutes, medium-high cost)
      - Multi-site active-active (RTO: seconds, high cost)
    - Geographic redundancy across datacenters
    - Cross-region replication in cloud (AWS Multi-AZ, Azure Availability Zones)
    - DR testing procedures and failover drills

12. Real-world implementation examples:
    - Linux HA cluster: Web server failover with Pacemaker
    - Windows Failover Cluster: SQL Server AlwaysOn
    - Kubernetes HA: 3-node control plane setup
    - MySQL master-slave replication with automatic failover (MHA)
    - PostgreSQL Patroni cluster (3-node etcd + 3 database nodes)
    - Redis Sentinel for cache high availability
    - Complete configuration files and deployment scripts

13. Monitoring and alerting:
    - Health check strategies (TCP, HTTP, application-specific)
    - Metrics collection: uptime, failover count, replication lag
    - Alerting on failure events
    - Log aggregation (ELK, Splunk)
    - Chaos engineering: intentional failure injection

14. Best practices:
    - Eliminate single points of failure (SPOF)
    - Automate failover procedures
    - Regular DR testing (quarterly/annual)
    - Documentation and runbooks
    - Capacity planning for peak load during failover
    - Avoiding common pitfalls:
      - Split-brain scenarios
      - Insufficient testing
      - Over-engineering (cost vs. benefit)
      - Ignoring network as SPOF

15. Cost analysis:
    - TCO (Total Cost of Ownership) for different HA levels
    - Cloud vs. on-premise HA solutions
    - Reserved capacity for failover

Format: Bilingual (English first, Chinese second), include architecture diagrams, configuration files, command examples, availability calculations, and cost-benefit analyses.
Target audience: System administrators, DevOps engineers, solution architects, and IT managers responsible for mission-critical infrastructure.

作为高可用系统架构师和可靠性工程师，创建一份关于计算机系统配置方法（双份、双重、热备份、容错、集群）的全面技术文档，包括：

（包含上述所有15个要点的中文版本）

格式：双语（英文在前，中文在后），包含架构图、配置文件、命令示例、可用性计算和成本效益分析。
目标受众：系统管理员、DevOps工程师、解决方案架构师和负责任务关键型基础设施的IT经理。
```
