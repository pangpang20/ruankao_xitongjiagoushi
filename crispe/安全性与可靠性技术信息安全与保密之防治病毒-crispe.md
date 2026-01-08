# CRISPE提示词：安全性与可靠性技术信息安全与保密之防治病毒

## C (Capacity and Role) - 能力与角色
你是一位资深的网络安全专家、恶意软件分析师和软考系统架构设计师考试顾问，精通计算机病毒原理、恶意软件检测技术、反病毒策略、安全防护体系和应急响应机制。你在企业级安全防护方案设计、病毒事件响应、安全审计、漏洞评估和安全架构规划方面拥有丰富的实践经验，熟悉各类恶意软件（病毒、蠕虫、木马、勒索软件、APT）的特征、传播机制、检测方法和防御措施。你深刻理解系统架构设计师考试的知识体系，能够从理论深度、工程实践和考试要点三个维度系统讲解计算机病毒防治的全貌。

## R (Requirement) - 任务要求
请创建一份全面的技术文档，系统性地讲解"安全性与可靠性技术信息安全与保密之防治病毒"，需要满足以下要求：

1. **内容完整性**：
   - 深入阐述计算机病毒的定义、分类、特征与发展历程
   - 系统介绍病毒的工作原理（感染机制、触发机制、破坏机制）
   - 详细讲解常见恶意软件类型（病毒、蠕虫、木马、勒索软件、间谍软件、Rootkit、APT）
   - 全面分析病毒检测技术（特征码检测、启发式检测、行为检测、沙箱技术、机器学习检测）
   - 深入阐述防病毒策略（预防、检测、清除、恢复）
   - 详细讲解反病毒软件架构与工作原理
   - 提供企业级病毒防护体系设计与最佳实践
   - 阐述应急响应流程与病毒事件处理

2. **结构规范**：
   - 采用清晰的章节结构（病毒概述、病毒原理、恶意软件类型、检测技术、防护策略、反病毒软件、企业防护、应急响应）
   - 每种技术包含：定义、原理、实现方法、优缺点、应用场景、实例分析
   - 提供病毒感染流程图、检测架构图、防护体系图、应急响应流程图

3. **双语要求**：
   - 全文采用中英文双语格式
   - 英文在前，中文在后
   - 专业术语必须标注中英文对照

4. **考试导向**：
   - 标注系统架构设计师考试的重点内容
   - 包含典型考点和常见题型分析
   - 提供记忆技巧和答题要点

## I (Information) - 背景信息
- **目标读者**：准备软考系统架构设计师考试的考生、网络安全工程师、系统管理员、信息安全官、IT经理
- **知识背景**：具备操作系统基础、了解文件系统、理解进程和内存管理概念
- **应用场景**：考试备考、企业安全防护、病毒事件响应、安全审计、合规检查、安全架构设计
- **考试重点**：
  - 计算机病毒定义与三大特征（传染性、隐蔽性、破坏性）
  - 病毒分类（按感染对象、按破坏性、按触发条件）
  - 病毒生命周期（潜伏、传播、触发、执行）
  - 常见恶意软件类型对比（病毒、蠕虫、木马、勒索软件）
  - 病毒检测技术（特征码、启发式、行为检测）
  - 沙箱技术原理
  - 反病毒软件架构（扫描引擎、特征库、实时监控、更新机制）
  - 防病毒策略（纵深防御、最小权限、定期更新、备份）
  - 应急响应流程（准备、检测、遏制、根除、恢复、总结）
  - 常见病毒攻击手法（宏病毒、引导区病毒、文件型病毒、网络蠕虫）

## S (Statement) - 风格要求
1. **专业性**：使用准确的安全术语和恶意软件分析语言
2. **系统性**：逻辑清晰，层次分明，理论与实践结合
3. **实用性**：结合实际病毒案例、检测方法、防护配置
4. **可读性**：语言简洁明了，图表清晰规范
5. **双语对照**：确保英文和中文翻译准确一致，专业术语标准化

## P (Process) - 步骤说明
按照以下结构组织文档内容：

### 第一部分：计算机病毒概述（Computer Virus Overview）
1. 病毒的定义与历史（Definition and History）
   - Fred Cohen定义（1983）
   - 病毒发展历程（1970s → 2020s）
   - 著名病毒案例（Morris蠕虫、Melissa、ILOVEYOU、WannaCry、Stuxnet）
2. 病毒的基本特征（Basic Characteristics）
   - 传染性（Infectivity）
   - 隐蔽性（Stealth）
   - 破坏性（Destructiveness）
   - 触发性（Triggering）
   - 潜伏性（Latency）
3. 病毒分类（Classification）
   - 按感染对象：引导区病毒、文件型病毒、宏病毒、脚本病毒
   - 按破坏性：良性病毒、恶性病毒
   - 按触发条件：定时炸弹、逻辑炸弹
   - 按传播方式：网络蠕虫、邮件病毒、U盘病毒

### 第二部分：病毒工作原理（Virus Working Principles）
1. 病毒结构（Virus Structure）
   - 感染模块（Infection Module）
   - 触发模块（Trigger Module）
   - 破坏模块（Payload Module）
   - 隐藏模块（Stealth Module）
2. 病毒生命周期（Virus Life Cycle）
   - 潜伏期（Dormant Phase）
   - 传播期（Propagation Phase）
   - 触发期（Triggering Phase）
   - 执行期（Execution Phase）
3. 感染机制（Infection Mechanisms）
   - 覆盖型感染（Overwriting）
   - 寄生型感染（Parasitic）
   - 伴随型感染（Companion）
   - 源代码感染（Source Code Infection）
4. 隐藏技术（Stealth Techniques）
   - 加密（Encryption）
   - 多态性（Polymorphism）
   - 变形技术（Metamorphism）
   - Rootkit技术

### 第三部分：常见恶意软件类型（Common Malware Types）
1. 计算机病毒（Computer Virus）
   - 定义与特征
   - 典型案例
2. 蠕虫（Worm）
   - 与病毒的区别
   - 传播机制
   - 典型案例（Morris、Conficker、WannaCry）
3. 木马（Trojan Horse）
   - 定义与工作原理
   - 远程访问木马（RAT）
   - 典型案例
4. 勒索软件（Ransomware）
   - 加密勒索原理
   - 支付机制（比特币）
   - 典型案例（WannaCry、Petya、CryptoLocker）
5. 间谍软件（Spyware）
   - 键盘记录器（Keylogger）
   - 屏幕捕获
   - 数据窃取
6. 广告软件（Adware）
7. Rootkit
   - 用户态Rootkit
   - 内核态Rootkit
   - 引导Rootkit
8. APT（Advanced Persistent Threat）高级持续威胁
   - 定义与特点
   - 攻击阶段
   - 典型案例（Stuxnet、APT1）

### 第四部分：病毒检测技术（Virus Detection Techniques）
1. 特征码检测（Signature-based Detection）
   - 原理与实现
   - 特征库管理
   - 优缺点
2. 启发式检测（Heuristic Detection）
   - 静态启发式
   - 动态启发式
   - 代码仿真
3. 行为检测（Behavior-based Detection）
   - 行为特征识别
   - 异常行为监控
   - HIPS（Host-based Intrusion Prevention System）
4. 沙箱技术（Sandbox Technology）
   - 虚拟化沙箱
   - 隔离执行
   - 行为分析
5. 完整性检查（Integrity Checking）
   - 文件校验和
   - 数字签名验证
   - HIDS（Host-based Intrusion Detection System）
6. 机器学习检测（Machine Learning Detection）
   - 特征工程
   - 分类算法
   - 深度学习应用

### 第五部分：反病毒软件（Antivirus Software）
1. 反病毒软件架构（Architecture）
   - 扫描引擎（Scan Engine）
   - 病毒特征库（Signature Database）
   - 实时监控模块（Real-time Monitor）
   - 更新模块（Update Module）
   - 隔离区（Quarantine）
2. 扫描技术（Scanning Techniques）
   - 按需扫描（On-demand Scan）
   - 实时扫描（Real-time Scan）
   - 计划扫描（Scheduled Scan）
   - 快速扫描vs完全扫描
3. 病毒清除（Virus Removal）
   - 隔离（Quarantine）
   - 删除（Delete）
   - 修复（Repair）
4. 主流反病毒软件对比
   - Windows Defender
   - Norton
   - Kaspersky
   - Avast
   - ClamAV（开源）

### 第六部分：防病毒策略（Antivirus Strategies）
1. 预防措施（Prevention）
   - 安装反病毒软件
   - 定期更新
   - 最小权限原则
   - 安全意识培训
   - 补丁管理
2. 检测与监控（Detection and Monitoring）
   - 实时监控
   - 定期扫描
   - 日志分析
   - 异常检测
3. 纵深防御（Defense in Depth）
   - 网络层防护（防火墙、IDS/IPS）
   - 主机层防护（反病毒、HIPS）
   - 应用层防护（输入验证、安全编码）
   - 数据层防护（加密、备份）
4. 备份与恢复（Backup and Recovery）
   - 3-2-1备份策略
   - 离线备份
   - 恢复测试

### 第七部分：企业病毒防护体系（Enterprise Virus Protection）
1. 安全架构设计（Security Architecture）
   - 边界防护
   - 终端防护
   - 邮件网关防护
   - Web过滤
2. 集中管理（Centralized Management）
   - 统一策略管理
   - 集中日志收集
   - 自动更新
   - 威胁情报共享
3. 安全策略（Security Policies）
   - 可接受使用策略（AUP）
   - 补丁管理策略
   - 数据分类与保护
   - 访问控制策略

### 第八部分：应急响应（Incident Response）
1. 应急响应流程（IR Process）
   - 准备（Preparation）
   - 检测与分析（Detection and Analysis）
   - 遏制（Containment）
   - 根除（Eradication）
   - 恢复（Recovery）
   - 总结与改进（Lessons Learned）
2. 病毒事件处理（Virus Incident Handling）
   - 隔离受感染系统
   - 识别病毒类型
   - 清除病毒
   - 系统恢复
   - 事后分析
3. 取证与分析（Forensics and Analysis）
   - 证据收集
   - 恶意软件逆向分析
   - 根因分析

### 第九部分：考试要点与案例分析
1. 历年考试重点题型
2. 典型病毒案例分析
3. 答题技巧与记忆要点

## E (Example) - 输出示例
提供以下内容格式：

```markdown
## 1. Computer Virus Overview | 计算机病毒概述

### 1.1 Definition and Characteristics | 定义与特征

**English:**

A **Computer Virus** is a self-replicating program that spreads by inserting copies of itself into other executable code or documents. It requires a host program to run and can cause damage to data, files, or system resources.

**Fred Cohen's Definition (1983)**:
"A computer virus is a program that can 'infect' other programs by modifying them to include a possibly evolved copy of itself."

**Three Key Characteristics | 三大关键特征**:

**1. Infectivity (传染性)**
- Self-replicating: Copies itself to other files
- Requires host program
- Spreads through user actions or automated mechanisms

**2. Stealth (隐蔽性)**
- Conceals presence from users and antivirus
- Uses encryption, polymorphism, rootkit techniques
- Mimics legitimate processes

**3. Destructiveness (破坏性)**
- Ranges from harmless (displaying messages) to catastrophic (data deletion)
- System slowdown, crashes, data corruption
- Denial of service, data theft

**中文:**

**计算机病毒**是一种自我复制的程序，通过将自身副本插入其他可执行代码或文档来传播。它需要宿主程序才能运行，并可能对数据、文件或系统资源造成损害。

**三大特征**: 传染性、隐蔽性、破坏性

**[Exam Focus | 考试重点]**: Understand Fred Cohen's definition, identify three key characteristics, differentiate from other malware types.

---

## 3. Common Malware Types | 常见恶意软件类型

### 3.1 Virus vs. Worm vs. Trojan | 病毒vs蠕虫vs木马

**Comparison Table | 对比表**:

| Aspect<br/>方面                         | Virus<br/>病毒               | Worm<br/>蠕虫                   | Trojan<br/>木马                 |
| --------------------------------------- | ---------------------------- | ------------------------------- | ------------------------------- |
| **Self-replication<br/>自我复制**       | Yes<br/>是                   | Yes<br/>是                      | No<br/>否                       |
| **Requires host<br/>需要宿主**          | Yes<br/>是                   | No<br/>否                       | No<br/>否                       |
| **User action needed<br/>需要用户操作** | Yes<br/>是                   | No<br/>否                       | Yes (initial)<br/>是（初始）    |
| **Spreads via<br/>传播方式**            | Infected files<br/>感染文件  | Network<br/>网络                | Social engineering<br/>社会工程 |
| **Primary harm<br/>主要危害**           | Data corruption<br/>数据破坏 | Network congestion<br/>网络拥塞 | Backdoor access<br/>后门访问    |

**[Exam Focus | 考试重点]**: 
- Memorize comparison table
- Identify malware type from scenario descriptions
- Understand propagation mechanisms

---

## 4. Detection Techniques | 检测技术

### 4.1 Signature-based vs. Heuristic Detection | 特征码检测vs启发式检测

**Signature-based Detection | 特征码检测**:

```
Process:
1. Extract signature from known virus
   从已知病毒中提取特征码
   
   Example: Unique byte sequence
   示例: 唯一的字节序列
   Signature: \x4D\x5A\x90\x00\x03...

2. Store in signature database
   存储在特征库中
   
3. Scan files for matching signatures
   扫描文件寻找匹配的特征码
   
   if (file contains signature):
       Flag as infected
       标记为已感染

Advantages:
✓ High accuracy (low false positives)
✓ Fast scanning
✓ Well-established technology

Disadvantages:
✗ Cannot detect new/unknown viruses (zero-day)
✗ Requires frequent updates
✗ Ineffective against polymorphic viruses

优势:
✓ 高准确性（低误报率）
✓ 快速扫描
✓ 成熟技术

劣势:
✗ 无法检测新病毒/未知病毒（零日）
✗ 需要频繁更新
✗ 对多态病毒无效
```

**Heuristic Detection | 启发式检测**:

```
Approach: Analyze code behavior and structure
方法: 分析代码行为和结构

Heuristic Rules:
启发式规则:

1. Suspicious API calls
   可疑的API调用
   - WriteFile() to system directories
   - RegistrySetValue() for auto-start

2. Code patterns
   代码模式
   - Self-modification
   - Encryption/decryption loops

3. File characteristics
   文件特征
   - Unusual entry points
   - Compressed/packed executables

Example:
if (writes to HKEY_RUN && modifies system files && encrypts data):
    Score += 80 (high risk)
    Likely ransomware
    可能是勒索软件

Advantages:
✓ Can detect new/unknown viruses
✓ Proactive protection

Disadvantages:
✗ Higher false positive rate
✗ Slower than signature-based
✗ May flag legitimate software

优势:
✓ 可检测新/未知病毒
✓ 主动防护

劣势:
✗ 较高误报率
✗ 比特征码检测慢
✗ 可能标记合法软件
```

**[Exam Focus | 考试重点]**: 
- Compare signature-based vs. heuristic detection
- Understand when each technique is effective
- Recognize limitations of signature-based (zero-day attacks)

---

## 5. Antivirus Software Architecture | 反病毒软件架构

```
┌────────────────────────────────────────────────────────┐
│           Antivirus Software Architecture              │
│           反病毒软件架构                               │
├────────────────────────────────────────────────────────┤
│                                                        │
│  ┌──────────────────────────────────────────────────┐ │
│  │         User Interface (UI)                      │ │
│  │         用户界面                                 │ │
│  │  - Scan controls                                 │ │
│  │  - Settings                                      │ │
│  │  - Quarantine management                         │ │
│  │  - 扫描控制                                      │ │
│  │  - 设置                                          │ │
│  │  - 隔离区管理                                    │ │
│  └──────────────────┬───────────────────────────────┘ │
│                     │                                  │
│  ┌──────────────────▼───────────────────────────────┐ │
│  │         Scan Engine (核心扫描引擎)               │ │
│  │                                                  │ │
│  │  ┌────────────┐  ┌────────────┐  ┌───────────┐ │ │
│  │  │Signature   │  │Heuristic   │  │ Behavior  │ │ │
│  │  │Detection   │  │Analysis    │  │ Monitoring│ │ │
│  │  │特征码检测  │  │启发式分析  │  │ 行为监控  │ │ │
│  │  └────────────┘  └────────────┘  └───────────┘ │ │
│  └──────────────────┬───────────────────────────────┘ │
│                     │                                  │
│  ┌──────────────────▼───────────────────────────────┐ │
│  │      Signature Database (病毒特征库)             │ │
│  │  - Virus signatures                              │ │
│  │  - Heuristic rules                               │ │
│  │  - Whitelisted files                             │ │
│  │  - 病毒特征码                                    │ │
│  │  - 启发式规则                                    │ │
│  │  - 白名单文件                                    │ │
│  └──────────────────┬───────────────────────────────┘ │
│                     │                                  │
│  ┌──────────────────▼───────────────────────────────┐ │
│  │      Real-time Monitor (实时监控模块)            │ │
│  │  - File system monitoring                        │ │
│  │  - Process monitoring                            │ │
│  │  - Network traffic inspection                    │ │
│  │  - 文件系统监控                                  │ │
│  │  - 进程监控                                      │ │
│  │  - 网络流量检查                                  │ │
│  └──────────────────┬───────────────────────────────┘ │
│                     │                                  │
│  ┌──────────────────▼───────────────────────────────┐ │
│  │         Update Module (更新模块)                 │ │
│  │  - Automatic updates                             │ │
│  │  - Incremental updates                           │ │
│  │  - Cloud-based threat intelligence               │ │
│  │  - 自动更新                                      │ │
│  │  - 增量更新                                      │ │
│  │  - 基于云的威胁情报                              │ │
│  └──────────────────┬───────────────────────────────┘ │
│                     │                                  │
│  ┌──────────────────▼───────────────────────────────┐ │
│  │         Quarantine (隔离区)                       │ │
│  │  - Isolated storage for infected files           │ │
│  │  - Encrypted container                           │ │
│  │  - Restore capability                            │ │
│  │  - 被感染文件的隔离存储                          │ │
│  │  - 加密容器                                      │ │
│  │  - 恢复能力                                      │ │
│  └──────────────────────────────────────────────────┘ │
└────────────────────────────────────────────────────────┘
```

**[Exam Focus | 考试重点]**: 
- Understand antivirus architecture components
- Recognize scan engine's role
- Explain update mechanism importance
- Identify quarantine function
```

**内容深度要求**：
- 每种恶意软件类型提供完整的定义、特征、传播机制、典型案例
- 每种检测技术提供详细的原理、实现方法、优缺点对比
- 反病毒软件架构包含完整的组件说明和工作流程
- 提供实际病毒案例分析（WannaCry、Stuxnet等）
- 包含企业级防护体系设计和应急响应流程
- 所有技术点必须关联考试要点
- 提供病毒防治决策树和最佳实践清单
