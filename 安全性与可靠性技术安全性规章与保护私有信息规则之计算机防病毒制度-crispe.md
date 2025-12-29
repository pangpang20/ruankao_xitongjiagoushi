# CRISPE提示词：安全性与可靠性技术安全性规章与保护私有信息规则之计算机防病毒制度

## C (Capacity and Role) - 能力与角色
你是一位资深的信息安全专家、网络安全工程师和软考系统架构设计师考试顾问，精通计算机病毒防护、恶意代码分析、病毒防护法规、安全策略制定和应急响应机制。你在病毒检测技术、防病毒软件架构、企业安全防护体系建设、安全合规管理和病毒事件处置方面拥有丰富的实践经验，熟悉各类恶意代码（病毒、蠕虫、木马、勒索软件、间谍软件）、防护技术（特征检测、行为检测、沙箱技术、启发式扫描）和防病毒管理制度。你深刻理解系统架构设计师考试的知识体系，能够从技术原理、法规制度和考试要点三个维度系统讲解计算机防病毒制度的全貌。

## R (Requirement) - 任务要求
请创建一份全面的技术文档，系统性地讲解"安全性与可靠性技术安全性规章与保护私有信息规则之计算机防病毒制度"，需要满足以下要求：

1. **内容完整性**：
   - 深入阐述计算机病毒的基本概念、分类与危害
   - 系统介绍恶意代码的类型（病毒、蠕虫、木马、勒索软件、间谍软件、僵尸网络）
   - 详细讲解病毒防护技术（特征检测、行为检测、启发式扫描、沙箱隔离、主动防御）
   - 全面分析中国计算机病毒防治法规与管理办法
   - 深入阐述企业防病毒管理制度（组织架构、技术措施、应急响应、培训教育）
   - 详细讲解防病毒软件的工作原理与架构
   - 提供病毒事件应急响应流程与最佳实践
   - 阐述病毒预防的技术手段与管理措施

2. **结构规范**：
   - 采用清晰的章节结构（病毒概述、恶意代码分类、防护技术、法规制度、管理体系、应急响应、技术实现）
   - 每种技术包含：定义、原理、分类、实现方法、优缺点、应用场景、实例分析
   - 提供防病毒架构图、病毒传播流程图、应急响应流程图、检测引擎架构图

3. **双语要求**：
   - 全文采用中英文双语格式
   - 英文在前，中文在后
   - 专业术语必须标注中英文对照

4. **考试导向**：
   - 标注系统架构设计师考试的重点内容
   - 包含典型考点和常见题型分析
   - 提供记忆技巧和答题要点

## I (Information) - 背景信息
- **目标读者**：准备软考系统架构设计师考试的考生、系统架构师、信息安全工程师、网络管理员、技术主管
- **知识背景**：具备操作系统基础、了解网络安全、理解软件工程概念
- **应用场景**：考试备考、企业防病毒体系建设、安全合规管理、应急响应规划、防病毒软件选型
- **考试重点**：
  - 计算机病毒的定义与特征（传染性、潜伏性、隐蔽性、破坏性、可触发性）
  - 恶意代码分类（病毒vs蠕虫vs木马vs勒索软件）
  - 病毒检测技术（特征码、行为分析、启发式、沙箱）
  - 中国计算机病毒防治管理办法
  - 防病毒软件架构（扫描引擎、病毒库、监控模块、更新机制）
  - 企业防病毒三层防护体系（网络层、主机层、应用层）
  - 病毒事件应急响应流程（检测、隔离、清除、恢复、分析）
  - 防病毒管理制度（病毒库更新、定期扫描、安全培训、访问控制）
  - 勒索软件防护策略（数据备份、权限控制、邮件过滤、补丁管理）

## S (Statement) - 风格要求
1. **专业性**：使用准确的信息安全术语和病毒防护技术语言
2. **系统性**：逻辑清晰，层次分明，理论与实践结合
3. **实用性**：结合实际防护案例、架构图、配置示例
4. **可读性**：语言简洁明了，图表清晰规范
5. **双语对照**：确保英文和中文翻译准确一致，专业术语标准化

## P (Process) - 步骤说明
按照以下结构组织文档内容：

### 第一部分：计算机病毒概述（Computer Virus Overview）
1. 病毒的定义与历史（Definition and History）
   - Fred Cohen定义（1983）：能够"感染"其他程序的程序
   - 病毒发展历史（从Boot病毒到现代APT）
   - 病毒危害与影响（经济损失、数据泄露、业务中断）
2. 病毒的基本特征（Basic Characteristics）**[考试重点]**
   - 传染性（Infectivity）- 自我复制能力
   - 潜伏性（Latency）- 等待触发条件
   - 隐蔽性（Concealment）- 避免被发现
   - 破坏性（Destructiveness）- 损害系统或数据
   - 可触发性（Triggerable）- 特定条件激活
3. 病毒的生命周期（Virus Life Cycle）
   - 感染阶段（Infection）
   - 潜伏阶段（Incubation）
   - 触发阶段（Triggering）
   - 发作阶段（Execution）
   - 传播阶段（Propagation）

### 第二部分：恶意代码分类（Malware Classification）**[考试重点]**
1. 计算机病毒（Computer Virus）
   - 文件病毒（File Infector）
   - 引导扇区病毒（Boot Sector Virus）
   - 宏病毒（Macro Virus）
   - 脚本病毒（Script Virus）
2. 蠕虫（Worm）
   - 定义：独立传播，无需宿主文件
   - 传播方式（网络漏洞、电子邮件、即时通讯）
   - 典型案例（Melissa、ILOVEYOU、Conficker、WannaCry）
3. 木马（Trojan Horse）
   - 定义：伪装成合法软件，执行恶意功能
   - 类型（远程访问木马RAT、下载器、键盘记录器）
   - 与病毒的区别（不自我复制）
4. 勒索软件（Ransomware）
   - 加密勒索（Crypto Ransomware）
   - 锁屏勒索（Locker Ransomware）
   - 典型案例（WannaCry、NotPetya、Ryuk）
5. 间谍软件（Spyware）
   - 广告软件（Adware）
   - 键盘记录器（Keylogger）
   - 浏览器劫持（Browser Hijacker）
6. 僵尸网络（Botnet）
   - C&C服务器（Command and Control）
   - DDoS攻击
   - 垃圾邮件发送
7. Rootkit
   - 用户态Rootkit
   - 内核态Rootkit
   - 隐藏技术

### 第三部分：病毒检测与防护技术（Virus Detection and Protection）
1. 特征码检测（Signature-Based Detection）
   - 病毒特征库（Virus Signature Database）
   - 匹配算法（Hash、Pattern Matching）
   - 优点：准确率高、误报率低
   - 缺点：无法检测零日攻击
2. 行为检测（Behavior-Based Detection）
   - 异常行为监控（API调用、文件操作、注册表修改）
   - 沙箱技术（Sandbox）
   - 虚拟机执行（Virtual Machine Execution）
3. 启发式扫描（Heuristic Scanning）
   - 静态启发式（Static Heuristic）- 代码模式分析
   - 动态启发式（Dynamic Heuristic）- 运行时行为分析
   - 规则引擎（Rule Engine）
4. 主动防御（Proactive Defense）
   - HIPS（Host-based Intrusion Prevention System）
   - 应用白名单（Application Whitelisting）
   - 系统加固（System Hardening）
5. 云安全技术（Cloud Security）
   - 云查询（Cloud Lookup）
   - 威胁情报（Threat Intelligence）
   - 大数据分析（Big Data Analytics）
6. 机器学习检测（Machine Learning Detection）
   - 监督学习（Supervised Learning）
   - 无监督学习（Unsupervised Learning）
   - 深度学习（Deep Learning）

### 第四部分：中国计算机病毒防治法规（China's Anti-Virus Regulations）
1. 法律法规体系（Legal Framework）
   - 网络安全法（Cybersecurity Law）- 第二十一条
   - 计算机病毒防治管理办法（2000年发布，2013年修订）
   - 信息安全技术标准（GB/T 18019）
2. 计算机病毒防治管理办法核心条款（Core Provisions）
   - 第六条：单位应当建立计算机病毒防治管理制度
   - 第七条：任何单位和个人不得制作、销售、传播计算机病毒
   - 第八条：从事计算机病毒防治产品生产的单位应当符合条件
   - 第九条：不得销售、出租含病毒的计算机软件和硬件
3. 防病毒产品管理（Anti-Virus Product Management）
   - 产品检测认证（Product Testing and Certification）
   - 市场准入要求（Market Access Requirements）
   - 病毒库更新义务（Signature Database Update Obligation）
4. 违规处罚（Penalties）
   - 行政处罚（警告、罚款、停业整顿）
   - 刑事责任（破坏计算机信息系统罪）

### 第五部分：企业防病毒管理制度（Enterprise Anti-Virus Management）
1. 组织架构（Organizational Structure）
   - 信息安全领导小组（Information Security Leadership Group）
   - 安全管理员（Security Administrator）
   - 应急响应团队（Emergency Response Team）
2. 技术防护体系（Technical Protection System）
   - 网络层防护（Network Layer）- 防火墙、IDS/IPS、网关防病毒
   - 主机层防护（Host Layer）- 终端防病毒、操作系统加固
   - 应用层防护（Application Layer）- 邮件过滤、Web过滤
3. 管理制度（Management Policies）
   - 病毒库更新制度（Signature Update Policy）
   - 定期扫描制度（Regular Scanning Policy）
   - 补丁管理制度（Patch Management Policy）
   - 安全培训制度（Security Training Policy）
   - 移动存储管理（Removable Media Management）
   - 电子邮件安全（Email Security）
   - 下载与安装管理（Download and Installation Management）
4. 应急响应机制（Emergency Response Mechanism）
   - 病毒事件分类分级（Incident Classification）
   - 应急响应流程（Response Procedures）
   - 恢复与总结（Recovery and Lessons Learned）

### 第六部分：病毒事件应急响应（Virus Incident Response）
1. 检测与报告（Detection and Reporting）
   - 自动检测（Automatic Detection）
   - 人工发现（Manual Discovery）
   - 报告流程（Reporting Procedure）
2. 隔离与遏制（Isolation and Containment）
   - 网络隔离（Network Isolation）
   - 主机隔离（Host Isolation）
   - 账户禁用（Account Disabling）
3. 清除与恢复（Eradication and Recovery）
   - 病毒清除（Virus Removal）
   - 系统重装（System Reinstallation）
   - 数据恢复（Data Recovery）
   - 业务恢复（Business Recovery）
4. 事后分析（Post-Incident Analysis）
   - 根因分析（Root Cause Analysis）
   - 改进措施（Improvement Measures）
   - 知识库更新（Knowledge Base Update）

### 第七部分：防病毒软件架构与实现（Anti-Virus Software Architecture）
1. 核心组件（Core Components）
   - 扫描引擎（Scanning Engine）
   - 病毒库（Virus Database）
   - 实时监控（Real-time Monitor）
   - 更新模块（Update Module）
   - 隔离区（Quarantine）
2. 扫描技术（Scanning Techniques）
   - 全盘扫描（Full Scan）
   - 快速扫描（Quick Scan）
   - 自定义扫描（Custom Scan）
   - 开机扫描（Boot Scan）
3. 更新机制（Update Mechanism）
   - 增量更新（Incremental Update）
   - 全量更新（Full Update）
   - 自动更新（Automatic Update）
   - 离线更新（Offline Update）
4. 性能优化（Performance Optimization）
   - 白名单技术（Whitelist）
   - 缓存机制（Cache）
   - 多线程扫描（Multi-threaded Scanning）
   - 云查询加速（Cloud Lookup Acceleration）

### 第八部分：勒索软件防护专题（Ransomware Protection）
1. 勒索软件攻击链（Ransomware Kill Chain）
   - 初始入侵（Initial Access）
   - 权限提升（Privilege Escalation）
   - 横向移动（Lateral Movement）
   - 数据加密（Data Encryption）
   - 勒索要求（Ransom Demand）
2. 防护策略（Protection Strategies）
   - 数据备份（Data Backup）- 3-2-1规则
   - 权限最小化（Least Privilege）
   - 邮件过滤（Email Filtering）
   - 补丁管理（Patch Management）
   - 网络隔离（Network Segmentation）
   - 用户培训（User Training）
3. 应对措施（Response Measures）
   - 不支付赎金（Do Not Pay Ransom）
   - 隔离感染主机（Isolate Infected Hosts）
   - 启动备份恢复（Restore from Backup）
   - 报告执法机关（Report to Law Enforcement）

### 第九部分：最佳实践与案例分析（Best Practices and Case Studies）
1. 防病毒最佳实践（Anti-Virus Best Practices）
   - 多层防御（Defense in Depth）
   - 定期评估（Regular Assessment）
   - 持续监控（Continuous Monitoring）
   - 快速响应（Rapid Response）
2. 典型案例分析（Case Studies）
   - WannaCry勒索软件事件（2017）
   - Conficker蠕虫事件（2008）
   - CryptoLocker勒索软件（2013）
   - 企业防病毒体系建设案例
3. 常见错误与教训（Common Mistakes and Lessons）
   - 忽视病毒库更新
   - 缺乏数据备份
   - 权限管理不当
   - 安全意识薄弱

### 第十部分：考试要点与答题技巧（Exam Focus and Techniques）
1. 高频考点总结
   - 病毒五大特征（传染、潜伏、隐蔽、破坏、可触发）
   - 病毒vs蠕虫vs木马对比
   - 特征检测vs行为检测vs启发式扫描
   - 计算机病毒防治管理办法核心条款
   - 企业防病毒三层防护体系
   - 应急响应流程
2. 典型题型分析
   - 恶意代码分类题
   - 检测技术对比题
   - 法规条款应用题
   - 防护架构设计题
   - 应急响应流程题
3. 答题技巧
   - 特征记忆法（病毒五特征口诀）
   - 对比表格法（病毒vs蠕虫vs木马）
   - 流程图记忆法（应急响应流程）

## E (Example) - 输出示例

### 示例1：病毒五大特征

```markdown
## Five Characteristics of Computer Virus | 计算机病毒五大特征 **[Exam Focus | 考试重点]**

**English:**

1. **Infectivity (传染性)**
   - Ability to replicate itself and infect other programs or files
   - 能够自我复制并感染其他程序或文件

2. **Latency (潜伏性)**
   - Can hide in the system waiting for trigger conditions
   - 可以隐藏在系统中等待触发条件

3. **Concealment (隐蔽性)**
   - Uses various techniques to avoid detection
   - 使用各种技术避免被检测

4. **Destructiveness (破坏性)**
   - Causes damage to data, programs, or hardware
   - 对数据、程序或硬件造成损害

5. **Triggerable (可触发性)**
   - Activates under specific conditions (date, event, command)
   - 在特定条件下激活（日期、事件、命令）

**Memory Aid | 记忆口诀**: **传潜隐破触**

**中文:**

计算机病毒的五大基本特征是考试高频考点，必须熟练掌握。
```

### 示例2：病毒vs蠕虫vs木马对比

```markdown
## Malware Comparison | 恶意代码对比 **[Exam Focus | 考试重点]**

| Feature<br/>特征                  | Virus<br/>病毒                               | Worm<br/>蠕虫                         | Trojan<br/>木马                         |
| --------------------------------- | -------------------------------------------- | ------------------------------------- | --------------------------------------- |
| **Self-replication<br/>自我复制** | Yes (needs host file)<br/>是（需要宿主文件） | Yes (standalone)<br/>是（独立存在）   | No<br/>否                               |
| **Propagation<br/>传播方式**      | Infects files<br/>感染文件                   | Network exploitation<br/>网络漏洞利用 | Social engineering<br/>社会工程学       |
| **Host required<br/>需要宿主**    | Yes<br/>是                                   | No<br/>否                             | No<br/>否                               |
| **Typical harm<br/>典型危害**     | File corruption<br/>文件损坏                 | Network congestion<br/>网络拥塞       | Data theft, backdoor<br/>数据窃取、后门 |
| **Example<br/>示例**              | Melissa<br/>梅丽莎病毒                       | Conficker<br/>震荡波                  | Zeus<br/>宙斯木马                       |
```

### 示例3：应急响应流程图

```
Virus Incident Response Process
病毒事件应急响应流程

┌─────────────────────────────────────────────────────────┐
│  Phase 1: Detection and Reporting (检测与报告)          │
│  ┌───────────────────────────────────────────────────┐ │
│  │ • Automatic alert from anti-virus software        │ │
│  │   防病毒软件自动告警                              │ │
│  │ • User report abnormal behavior                   │ │
│  │   用户报告异常行为                                │ │
│  │ • Report to security team immediately             │ │
│  │   立即报告安全团队                                │ │
│  └───────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────┐
│  Phase 2: Isolation and Containment (隔离与遏制)        │
│  ┌───────────────────────────────────────────────────┐ │
│  │ • Disconnect infected host from network           │ │
│  │   断开感染主机网络连接                            │ │
│  │ • Disable user accounts if compromised            │ │
│  │   禁用被入侵的用户账户                            │ │
│  │ • Block malicious IP/domain                       │ │
│  │   封锁恶意IP/域名                                 │ │
│  └───────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────┐
│  Phase 3: Eradication and Recovery (清除与恢复)         │
│  ┌───────────────────────────────────────────────────┐ │
│  │ • Run full system scan and remove virus           │ │
│  │   运行全盘扫描并清除病毒                          │ │
│  │ • Reinstall system if necessary                   │ │
│  │   必要时重装系统                                  │ │
│  │ • Restore data from clean backup                  │ │
│  │   从干净备份恢复数据                              │ │
│  │ • Update signatures and patches                   │ │
│  │   更新病毒库和补丁                                │ │
│  └───────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────┐
│  Phase 4: Post-Incident Analysis (事后分析)             │
│  ┌───────────────────────────────────────────────────┐ │
│  │ • Determine root cause                            │ │
│  │   确定根本原因                                    │ │
│  │ • Document lessons learned                        │ │
│  │   记录经验教训                                    │ │
│  │ • Update security policies                        │ │
│  │   更新安全策略                                    │ │
│  │ • Conduct security training                       │ │
│  │   开展安全培训                                    │ │
│  └───────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────┘
```

## 输出要求
1. 使用Markdown格式
2. 包含详细的技术原理、法规条款、实施案例
3. 提供清晰的架构图、流程图、对比表格
4. 标注考试重点内容
5. 包含真实病毒事件案例分析
6. 中英文双语对照，英文在前，中文在后
7. 每个重要概念提供定义、特征、实例
8. 提供防护实施的具体步骤和最佳实践
