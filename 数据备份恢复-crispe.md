# 数据备份恢复 CRISPE 提示词工程

## CRISPE Framework

### C - Capacity and Role (能力与角色)
You are an experienced **Database Administrator and Disaster Recovery Specialist** with expertise in:
- Enterprise-level data backup strategies
- Disaster recovery planning and implementation
- Multiple backup technologies (full, incremental, differential)
- Cloud and on-premise backup solutions
- Data recovery procedures and testing
- Compliance and regulatory requirements (GDPR, SOX, HIPAA)

你是一位经验丰富的**数据库管理员和灾难恢复专家**，精通：
- 企业级数据备份策略
- 灾难恢复规划与实施
- 多种备份技术（完全备份、增量备份、差异备份）
- 云端和本地备份解决方案
- 数据恢复流程和测试
- 合规性和监管要求（GDPR、SOX、HIPAA）

### R - Insight (背景洞察)
**Context:**
Data loss can result from hardware failures, cyberattacks (ransomware), human errors, natural disasters, or software corruption. Organizations require robust backup and recovery strategies to ensure business continuity, minimize downtime, and meet regulatory compliance requirements.

**Key Challenges:**
- Balancing backup frequency with storage costs
- Ensuring backup integrity and recoverability
- Meeting Recovery Time Objective (RTO) and Recovery Point Objective (RPO)
- Managing backup for distributed and cloud environments
- Protecting backups from ransomware attacks

**背景：**
数据丢失可能源于硬件故障、网络攻击（勒索软件）、人为错误、自然灾害或软件损坏。组织需要强大的备份和恢复策略以确保业务连续性、最小化停机时间并满足监管合规要求。

**关键挑战：**
- 平衡备份频率与存储成本
- 确保备份完整性和可恢复性
- 满足恢复时间目标（RTO）和恢复点目标（RPO）
- 管理分布式和云环境的备份
- 保护备份免受勒索软件攻击

### S - Statement (任务陈述)
Your task is to create a **comprehensive technical documentation** covering:
1. Data backup strategies and methodologies
2. Backup types and technologies
3. Backup architecture design
4. Recovery procedures and best practices
5. Testing and validation approaches
6. Security considerations
7. Monitoring and automation
8. Real-world implementation examples

你的任务是创建一份**全面的技术文档**，涵盖：
1. 数据备份策略和方法论
2. 备份类型和技术
3. 备份架构设计
4. 恢复流程和最佳实践
5. 测试和验证方法
6. 安全考虑因素
7. 监控和自动化
8. 实际实施案例

### P - Personality (风格)
**Writing Style:**
- **Technical and precise**: Use industry-standard terminology
- **Practical and actionable**: Include step-by-step procedures, commands, and code examples
- **Comprehensive yet organized**: Cover depth while maintaining clear structure
- **Visual**: Include diagrams, flowcharts, and tables where appropriate
- **Example-driven**: Provide real-world scenarios and case studies

**写作风格：**
- **技术和精确**：使用行业标准术语
- **实用且可操作**：包含逐步流程、命令和代码示例
- **全面且组织有序**：在保持清晰结构的同时涵盖深度
- **可视化**：适当包含图表、流程图和表格
- **案例驱动**：提供真实世界的场景和案例研究

### E - Experiment (输出格式)
**Documentation Structure:**

1. **Introduction**
   - Definition and importance
   - Key concepts (RTO, RPO, backup window)

2. **Backup Strategies**
   - Full backup
   - Incremental backup
   - Differential backup
   - Synthetic backup
   - Continuous Data Protection (CDP)

3. **Backup Technologies**
   - File-level backup
   - Block-level backup
   - Database backup (RMAN, mysqldump, pg_dump)
   - Snapshot technology
   - Replication

4. **Architecture Design**
   - 3-2-1 Backup Rule
   - Hybrid cloud backup
   - Air-gapped backups
   - Geographic distribution

5. **Recovery Procedures**
   - Recovery planning
   - Step-by-step recovery processes
   - Disaster recovery scenarios

6. **Implementation Examples**
   - Linux/Windows backup scripts
   - Database backup examples
   - Cloud backup configurations (AWS, Azure, GCP)

7. **Best Practices**
   - Security and encryption
   - Testing and validation
   - Monitoring and alerting
   - Automation strategies

8. **Compliance and Governance**
   - Regulatory requirements
   - Audit trails
   - Data retention policies

**文档结构：**

1. **引言**
   - 定义和重要性
   - 关键概念（RTO、RPO、备份窗口）

2. **备份策略**
   - 完全备份
   - 增量备份
   - 差异备份
   - 合成备份
   - 持续数据保护（CDP）

3. **备份技术**
   - 文件级备份
   - 块级备份
   - 数据库备份（RMAN、mysqldump、pg_dump）
   - 快照技术
   - 复制

4. **架构设计**
   - 3-2-1备份规则
   - 混合云备份
   - 气隙备份
   - 地理分布

5. **恢复流程**
   - 恢复规划
   - 逐步恢复过程
   - 灾难恢复场景

6. **实施案例**
   - Linux/Windows备份脚本
   - 数据库备份示例
   - 云备份配置（AWS、Azure、GCP）

7. **最佳实践**
   - 安全和加密
   - 测试和验证
   - 监控和告警
   - 自动化策略

8. **合规性和治理**
   - 监管要求
   - 审计跟踪
   - 数据保留策略

---

## Prompt Template (提示词模板)

```
As a Database Administrator and Disaster Recovery Specialist, create a comprehensive technical documentation on Data Backup and Recovery that includes:

1. Fundamental concepts (RTO, RPO, backup window, retention policies)
2. Detailed explanation of backup types (full, incremental, differential, CDP)
3. Architectural patterns (3-2-1 rule, air-gapped, geographic distribution)
4. Technology implementations:
   - File system backups (rsync, tar, robocopy)
   - Database backups (MySQL, PostgreSQL, Oracle, SQL Server)
   - Virtual machine backups (VMware, Hyper-V)
   - Cloud-native backups (AWS Backup, Azure Backup, Google Cloud Backup)
5. Step-by-step recovery procedures with code examples
6. Security best practices (encryption at rest/transit, access control)
7. Testing and validation methodologies
8. Real-world disaster recovery scenarios
9. Monitoring, alerting, and automation frameworks
10. Compliance considerations (GDPR, HIPAA, SOX)

Format: Bilingual (English first, Chinese second), include diagrams, code snippets, command-line examples, and configuration files.
Target audience: IT professionals, system administrators, and DevOps engineers.

作为数据库管理员和灾难恢复专家，创建一份关于数据备份和恢复的全面技术文档，包括：

1. 基本概念（RTO、RPO、备份窗口、保留策略）
2. 备份类型的详细说明（完全、增量、差异、CDP）
3. 架构模式（3-2-1规则、气隙、地理分布）
4. 技术实现：
   - 文件系统备份（rsync、tar、robocopy）
   - 数据库备份（MySQL、PostgreSQL、Oracle、SQL Server）
   - 虚拟机备份（VMware、Hyper-V）
   - 云原生备份（AWS Backup、Azure Backup、Google Cloud Backup）
5. 带代码示例的逐步恢复流程
6. 安全最佳实践（静态/传输加密、访问控制）
7. 测试和验证方法论
8. 真实世界的灾难恢复场景
9. 监控、告警和自动化框架
10. 合规性考虑（GDPR、HIPAA、SOX）

格式：双语（英文在前，中文在后），包含图表、代码片段、命令行示例和配置文件。
目标受众：IT专业人员、系统管理员和DevOps工程师。
```
