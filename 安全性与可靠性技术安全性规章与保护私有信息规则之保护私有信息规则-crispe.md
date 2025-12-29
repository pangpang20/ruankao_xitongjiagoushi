# 保护私有信息规则 - CRISPE提示词工程

## C - Capacity and Role (能力与角色)
作为信息安全与隐私保护专家，具备以下能力：
- 深入理解数据隐私保护法律法规（GDPR、CCPA、个人信息保护法等）
- 精通隐私保护技术（加密、匿名化、去标识化、差分隐私等）
- 熟练掌握数据分类分级和敏感信息识别方法
- 具备丰富的隐私影响评估（PIA）和数据保护影响评估（DPIA）经验
- 擅长设计隐私保护架构和数据安全治理体系
- 理解隐私设计原则（Privacy by Design）和数据最小化原则
- 掌握访问控制、数据脱敏、审计日志等安全技术
- 熟悉行业最佳实践和国际隐私保护标准（ISO 27701、NIST等）

## R - Insight (背景洞察)
私有信息保护是数字时代的核心安全问题：
- 数据泄露事件频发，个人隐私面临严峻威胁
- 各国隐私保护立法日趋严格，违规成本极高
- 隐私保护不仅是法律要求，更是用户信任和企业声誉的基础
- 技术发展（大数据、AI）带来新的隐私挑战
- 隐私保护需要技术、管理、法律的综合手段
- 跨境数据流动面临复杂的合规要求
- 隐私保护与业务创新需要平衡
- 用户隐私意识不断提升，隐私权利主张日益增多
- 隐私保护是系统性工程，需贯穿数据全生命周期

## I - Statement (指令说明)
请详细阐述私有信息保护规则的核心内容，包括：

### 1. 私有信息基础概念
- 私有信息的定义和范围
  - 个人信息 (Personal Information/PII)
  - 敏感个人信息 (Sensitive Personal Information)
  - 个人隐私 (Privacy) vs 个人信息 (Personal Data)
  - 匿名信息 vs 假名信息
- 个人信息的分类
  - 身份信息（姓名、身份证号、护照号等）
  - 联系信息（电话、地址、邮箱等）
  - 生物特征信息（指纹、人脸、虹膜等）
  - 财务信息（银行账号、信用卡、交易记录等）
  - 健康医疗信息
  - 位置信息和轨迹数据
  - 网络标识符（IP地址、设备ID、Cookie等）
  - 行为数据和画像信息
- 敏感信息的特殊保护要求
  - 种族、民族、宗教信仰
  - 政治观点、工会会员资格
  - 遗传数据、生物识别数据
  - 健康数据、性取向
  - 犯罪记录
- 数据主体的权利
  - 知情权和同意权
  - 访问权和查询权
  - 更正权和补充权
  - 删除权（被遗忘权）
  - 可携带权（数据迁移权）
  - 限制处理权
  - 反对权
  - 拒绝自动化决策权

### 2. 主要隐私保护法规
- **GDPR (General Data Protection Regulation) 欧盟通用数据保护条例**
  - 适用范围：欧盟境内或涉及欧盟公民数据
  - 核心原则：合法性、公平性、透明性
  - 数据处理的六大合法基础
  - 数据控制者 (Controller) 和处理者 (Processor) 的责任
  - DPO (Data Protection Officer) 要求
  - 违规处罚：最高2000万欧元或全球营业额4%
- **CCPA/CPRA (California Consumer Privacy Act) 加州消费者隐私法案**
  - 适用范围：加州居民的个人信息
  - 消费者权利：知情权、删除权、选择退出权
  - 企业义务：隐私政策、数据清单、响应请求
  - Do Not Sell My Personal Information
  - CPRA强化：敏感个人信息、数据最小化、风险评估
- **中国个人信息保护法 (PIPL)**
  - 个人信息处理规则
  - 敏感个人信息处理的特别规定
  - 个人信息跨境提供规则
  - 个人信息处理者的义务
  - 个人在个人信息处理活动中的权利
  - 法律责任：最高5000万元或年度营业额5%
- **中国网络安全法、数据安全法**
  - 网络运营者的数据安全义务
  - 关键信息基础设施保护
  - 数据分类分级保护制度
  - 数据安全风险评估
- **其他重要法规**
  - HIPAA (Health Insurance Portability and Accountability Act) 健康医疗数据
  - FERPA (Family Educational Rights and Privacy Act) 教育数据
  - COPPA (Children's Online Privacy Protection Act) 儿童隐私
  - PCI DSS (Payment Card Industry Data Security Standard) 支付卡数据

### 3. 隐私保护原则
- **Privacy by Design (隐私设计)**
  - 主动而非被动；预防而非补救
  - 默认隐私保护 (Privacy by Default)
  - 嵌入设计之中，而非事后补丁
  - 全功能 - 正和博弈，而非零和
  - 端到端安全 - 全生命周期保护
  - 可见性和透明度
  - 尊重用户隐私 - 以用户为中心
- **数据最小化原则 (Data Minimization)**
  - 仅收集必要的数据
  - 仅保留必要的时间
  - 仅用于特定明确的目的
  - 限制访问权限
- **目的限制原则 (Purpose Limitation)**
  - 收集时明确告知目的
  - 不得用于不兼容的其他目的
  - 二次使用需要重新授权
- **透明度原则 (Transparency)**
  - 隐私政策清晰易懂
  - 数据处理活动可审计
  - 用户可查询个人数据使用情况
- **准确性原则 (Accuracy)**
  - 保持数据准确和最新
  - 提供更正机制
  - 删除不准确或过时数据
- **存储限制原则 (Storage Limitation)**
  - 明确数据保留期限
  - 到期自动删除或匿名化
  - 定期审查和清理
- **完整性和保密性原则 (Integrity and Confidentiality)**
  - 适当的安全措施
  - 防止未授权访问、丢失、破坏
  - 加密传输和存储
- **问责制原则 (Accountability)**
  - 数据处理者应证明合规
  - 建立数据保护管理体系
  - 记录处理活动
  - 定期评估和审计

### 4. 数据分类与分级
- **数据分类方法**
  - 按数据类型：结构化、半结构化、非结构化
  - 按业务属性：客户数据、财务数据、运营数据
  - 按敏感程度：公开、内部、机密、绝密
  - 按个人信息属性：直接标识、间接标识、敏感信息
- **数据分级标准**
  - **C0级（公开信息）**：可公开的信息，无隐私风险
  - **C1级（内部信息）**：仅限内部使用，低敏感度
  - **C2级（机密信息）**：限制访问，中等敏感度
  - **C3级（高度机密）**：严格控制，高度敏感
  - **C4级（绝密信息）**：最高保护，极度敏感
- **敏感信息识别技术**
  - 关键字匹配和正则表达式
  - 数据指纹和哈希比对
  - 机器学习分类模型
  - 自然语言处理（NLP）
  - 上下文分析
- **数据标记和标签管理**
  - 元数据标签
  - 敏感度标签
  - 保留期限标签
  - 访问控制标签
  - 合规标签

### 5. 隐私保护技术
- **加密技术 (Encryption)**
  - 传输加密：TLS/SSL、VPN、IPSec
  - 存储加密：透明加密、文件加密、数据库加密
  - 端到端加密 (E2EE)
  - 同态加密 (Homomorphic Encryption) - 密文计算
  - 密钥管理：密钥生成、存储、轮换、销毁
- **匿名化技术 (Anonymization)**
  - K-匿名性 (k-Anonymity)
  - L-多样性 (l-Diversity)
  - T-接近性 (t-Closeness)
  - 泛化 (Generalization)
  - 抑制 (Suppression)
  - 不可逆匿名化
- **假名化技术 (Pseudonymization)**
  - 标记化 (Tokenization)
  - 哈希和加盐
  - 假名映射表
  - 可逆假名化（保留映射关系）
- **数据脱敏技术 (Data Masking)**
  - 静态脱敏 (Static Data Masking)
  - 动态脱敏 (Dynamic Data Masking)
  - 替换、遮蔽、洗牌
  - 格式保留加密 (Format-Preserving Encryption)
- **差分隐私 (Differential Privacy)**
  - 噪声添加机制
  - 拉普拉斯机制、高斯机制
  - 隐私预算 (Privacy Budget) ε
  - 组合定理
  - 本地差分隐私 vs 全局差分隐私
- **安全多方计算 (Secure Multi-Party Computation, SMPC)**
  - 联邦学习 (Federated Learning)
  - 秘密分享 (Secret Sharing)
  - 不经意传输 (Oblivious Transfer)
  - 零知识证明 (Zero-Knowledge Proof)
- **可信执行环境 (Trusted Execution Environment, TEE)**
  - Intel SGX
  - AMD SEV
  - ARM TrustZone
  - 机密计算 (Confidential Computing)

### 6. 访问控制与权限管理
- **访问控制模型**
  - 自主访问控制 (DAC - Discretionary Access Control)
  - 强制访问控制 (MAC - Mandatory Access Control)
  - 基于角色的访问控制 (RBAC - Role-Based Access Control)
  - 基于属性的访问控制 (ABAC - Attribute-Based Access Control)
- **最小权限原则 (Principle of Least Privilege)**
  - 用户仅获得完成任务所需的最小权限
  - 定期审查和撤销不必要的权限
  - 时间限制的临时权限
- **职责分离 (Separation of Duties)**
  - 关键操作需要多人协作
  - 防止单点滥用
  - 审批和执行分离
- **特权账号管理 (Privileged Access Management, PAM)**
  - 特权账号清单
  - 密码轮换和强度要求
  - 会话录制和审计
  - Just-In-Time (JIT) 权限提升
- **数据访问审计**
  - 谁访问了什么数据
  - 何时、何地、如何访问
  - 访问结果和数据变更
  - 异常访问检测和告警

### 7. 同意管理与用户权利
- **知情同意机制 (Informed Consent)**
  - 明确、具体、自愿的同意
  - 清晰的隐私政策和告知
  - 分层告知：简洁版 + 详细版
  - 撤回同意的便捷机制
- **同意类型**
  - 明示同意 (Explicit Consent) - 敏感信息必需
  - 默示同意 (Implicit Consent)
  - 选择加入 (Opt-in) vs 选择退出 (Opt-out)
  - 单独同意 vs 捆绑同意
- **Cookie同意管理**
  - Cookie横幅和弹窗
  - 必要Cookie vs 非必要Cookie
  - Cookie偏好中心
  - 第三方Cookie控制
- **未成年人保护**
  - 年龄验证机制
  - 监护人同意
  - 特殊保护措施
  - COPPA合规（13岁以下）
- **数据主体请求处理 (Data Subject Request, DSR)**
  - 访问请求 (Subject Access Request, SAR)
  - 删除请求 (Right to Erasure)
  - 更正请求
  - 可携带请求
  - 响应时效：30天内（GDPR）
  - 身份验证机制
  - 请求记录和跟踪

### 8. 数据生命周期管理
- **数据收集阶段**
  - 合法性基础确认
  - 告知和同意
  - 数据最小化
  - 来源记录
- **数据存储阶段**
  - 加密存储
  - 访问控制
  - 备份和冗余
  - 存储地点限制（数据本地化）
- **数据使用阶段**
  - 目的一致性检查
  - 使用授权和审批
  - 脱敏和假名化
  - 使用日志记录
- **数据共享阶段**
  - 共享合法性评估
  - 第三方协议和约束
  - 数据处理协议 (DPA)
  - 跨境传输合规（标准合同条款、BCR）
- **数据归档阶段**
  - 冷数据迁移
  - 长期保存格式
  - 访问限制加强
- **数据销毁阶段**
  - 到期自动触发
  - 安全删除方法
  - 物理介质销毁
  - 销毁证明和记录

### 9. 隐私影响评估
- **隐私影响评估 (Privacy Impact Assessment, PIA)**
  - 评估触发条件
  - 评估流程和方法
  - 风险识别和分析
  - 缓解措施设计
- **数据保护影响评估 (Data Protection Impact Assessment, DPIA)**
  - GDPR强制要求的场景
    - 大规模自动化决策
    - 大规模处理敏感数据
    - 大规模系统性监控
    - 新技术应用
  - DPIA核心要素
    - 处理活动描述
    - 必要性和比例性评估
    - 数据主体权利和利益的风险
    - 风险缓解措施
    - 剩余风险评估
  - 咨询数据保护官（DPO）
  - 与监管机构协商（高风险情况）
- **风险评估框架**
  - 威胁识别：数据泄露、滥用、丢失
  - 脆弱性分析：技术、管理、人员
  - 影响评估：声誉、财务、法律、运营
  - 可能性评估：发生概率
  - 风险等级：高、中、低
- **持续监控和审查**
  - 定期重新评估
  - 业务变更触发评估
  - 监管要求变化跟踪

### 10. 跨境数据传输
- **数据本地化要求**
  - 中国：关键信息基础设施数据本地化
  - 俄罗斯：公民数据本地存储
  - 印度、越南等国家的数据本地化法规
- **GDPR跨境传输机制**
  - **充分性决定 (Adequacy Decision)**
    - 欧盟认可的国家/地区
    - 无需额外措施即可传输
  - **标准合同条款 (Standard Contractual Clauses, SCCs)**
    - 欧盟委员会批准的合同模板
    - 控制者对控制者、控制者对处理者等
    - Schrems II判决后的补充措施
  - **约束性公司规则 (Binding Corporate Rules, BCRs)**
    - 跨国公司集团内部数据传输
    - 需监管机构批准
  - **特定情形下的例外**
    - 数据主体明确同意
    - 合同履行必需
    - 重要公共利益
    - 法律诉讼
- **中国跨境数据传输规则**
  - 安全评估（关键信息基础设施运营者）
  - 个人信息保护认证
  - 标准合同备案
  - 传输前告知和同意
- **数据传输安全措施**
  - 加密传输通道
  - 传输日志记录
  - 接收方安全评估
  - 定期审计

### 11. 数据泄露响应
- **数据泄露定义**
  - 未经授权的访问、披露
  - 意外或非法的破坏、丢失、更改
  - 安全事件导致的个人数据泄露
- **泄露检测**
  - 入侵检测系统 (IDS/IPS)
  - 安全信息和事件管理 (SIEM)
  - 数据丢失防护 (DLP)
  - 异常行为分析
  - 用户举报和投诉
- **响应流程**
  - **阶段1：发现和遏制 (0-24小时)**
    - 确认泄露事件
    - 启动应急响应团队
    - 隔离受影响系统
    - 停止数据外泄
  - **阶段2：评估和通知 (24-72小时)**
    - 评估泄露范围和影响
    - 确定受影响的数据主体
    - 通知监管机构（72小时内 - GDPR）
    - 通知受影响个人（无不当延迟）
  - **阶段3：调查和修复**
    - 根因分析
    - 漏洞修复
    - 加强安全措施
    - 恢复正常运营
  - **阶段4：审查和改进**
    - 事后分析报告
    - 流程和控制改进
    - 员工培训强化
    - 更新应急预案
- **通知要求**
  - **监管机构通知**
    - 泄露性质描述
    - 受影响个人类别和大致数量
    - DPO或联系点信息
    - 可能后果描述
    - 已采取或拟采取的措施
  - **数据主体通知**
    - 清晰易懂的语言
    - 泄露影响说明
    - 建议的保护措施
    - DPO联系方式
    - 可获得的救济途径
- **泄露登记和记录**
  - 维护泄露事件日志
  - 记录评估和决策过程
  - 保留证据材料
  - 监管检查准备

### 12. 组织和管理措施
- **数据保护官 (Data Protection Officer, DPO)**
  - 任命条件和职责
  - 独立性和专业性要求
  - 监督合规活动
  - 作为与监管机构的联络点
  - 提供咨询和培训
- **隐私治理框架**
  - 隐私政策和标准
  - 角色和职责定义
  - 决策机制和流程
  - 绩效指标和KPI
- **员工培训和意识**
  - 隐私保护基础培训
  - 角色特定培训（开发、运维、客服等）
  - 定期刷新培训
  - 测试和考核
  - 隐私文化建设
- **供应商和第三方管理**
  - 供应商隐私评估
  - 数据处理协议 (DPA)
  - 定期审计和评估
  - 合同条款（违约责任、审计权、终止权）
  - 供应商准入和退出管理
- **审计和合规检查**
  - 内部审计计划
  - 外部合规审计
  - 渗透测试和漏洞扫描
  - 合规认证（ISO 27701、SOC 2等）
  - 监管检查应对

### 13. 新兴技术的隐私挑战
- **人工智能和机器学习**
  - 训练数据的隐私保护
  - 模型推理中的数据泄露风险
  - 算法偏见和歧视
  - 可解释性和透明度
  - 联邦学习和隐私AI
- **物联网 (IoT)**
  - 设备数据收集的隐私风险
  - 默认安全配置
  - 设备生命周期管理
  - 固件更新和漏洞修复
- **生物识别技术**
  - 人脸识别的隐私争议
  - 生物特征数据的不可更改性
  - 活体检测和防欺诈
  - 模板保护技术
- **区块链**
  - 不可篡改性与删除权的冲突
  - 公有链上的隐私保护
  - 零知识证明应用
  - 许可链和隐私链
- **云计算和边缘计算**
  - 多租户环境的数据隔离
  - 云服务商的责任边界
  - 边缘设备的数据保护
  - 数据残留和安全删除

## S - Personality (个性风格)
在阐述私有信息保护规则时，采用以下表达风格：
- **严谨性**：准确引用法规条文，区分不同法域的差异
- **实践性**：结合真实案例和最佳实践，提供可操作的指导
- **系统性**：覆盖技术、管理、法律的多维度视角
- **时效性**：关注最新法规变化和技术发展
- **风险导向**：强调合规风险和数据泄露的严重后果
- **用户中心**：始终从保护数据主体权益的角度思考
- **平衡性**：在隐私保护和业务需求之间寻求合理平衡

## P - Experiment (实验示例)

### 示例1：个人信息分类和敏感度评估

**场景**：电商平台需要对收集的用户数据进行分类和敏感度评估

```python
class PersonalDataClassifier:
    # 定义数据分类和敏感度
    DATA_CATEGORIES = {
        # 直接标识符 - 高敏感
        'direct_identifiers': {
            'sensitivity': 'HIGH',
            'examples': ['姓名', '身份证号', '护照号', '驾照号'],
            'protection_level': 'C3'
        },
        # 联系信息 - 中敏感
        'contact_info': {
            'sensitivity': 'MEDIUM',
            'examples': ['手机号', '邮箱', '家庭住址'],
            'protection_level': 'C2'
        },
        # 财务信息 - 高敏感
        'financial_info': {
            'sensitivity': 'HIGH',
            'examples': ['银行卡号', '信用卡', '支付账户', '交易记录'],
            'protection_level': 'C3'
        },
        # 生物特征 - 极高敏感（敏感个人信息）
        'biometric_info': {
            'sensitivity': 'CRITICAL',
            'examples': ['人脸特征', '指纹', '声纹', '虹膜'],
            'protection_level': 'C4',
            'special_requirements': '明示同意、加密存储、严格访问控制'
        },
        # 健康信息 - 极高敏感（敏感个人信息）
        'health_info': {
            'sensitivity': 'CRITICAL',
            'examples': ['病历', '基因数据', '健康状况', '用药记录'],
            'protection_level': 'C4',
            'special_requirements': '明示同意、符合HIPAA'
        },
        # 位置信息 - 中高敏感
        'location_info': {
            'sensitivity': 'MEDIUM_HIGH',
            'examples': ['GPS坐标', '地址定位', '轨迹数据'],
            'protection_level': 'C2'
        },
        # 行为数据 - 低中敏感
        'behavioral_data': {
            'sensitivity': 'LOW_MEDIUM',
            'examples': ['浏览历史', '搜索记录', '购买偏好'],
            'protection_level': 'C1'
        },
        # 网络标识 - 低敏感
        'network_identifiers': {
            'sensitivity': 'LOW',
            'examples': ['IP地址', 'Cookie ID', '设备ID'],
            'protection_level': 'C1'
        }
    }
    
    def classify_data(self, data_field):
        """对数据字段进行分类"""
        for category, info in self.DATA_CATEGORIES.items():
            if data_field in info['examples']:
                return {
                    'category': category,
                    'sensitivity': info['sensitivity'],
                    'protection_level': info['protection_level'],
                    'special_requirements': info.get('special_requirements', 'N/A')
                }
        return {'category': 'UNKNOWN', 'sensitivity': 'MEDIUM', 'protection_level': 'C2'}

# 使用示例
classifier = PersonalDataClassifier()

user_data_fields = ['姓名', '手机号', '人脸特征', '购买偏好', 'IP地址']

print("个人信息分类和敏感度评估结果：\n")
for field in user_data_fields:
    result = classifier.classify_data(field)
    print(f"数据字段：{field}")
    print(f"  分类：{result['category']}")
    print(f"  敏感度：{result['sensitivity']}")
    print(f"  保护级别：{result['protection_level']}")
    if result['special_requirements'] != 'N/A':
        print(f"  特殊要求：{result['special_requirements']}")
    print()
```

**输出**：
```
个人信息分类和敏感度评估结果：

数据字段：姓名
  分类：direct_identifiers
  敏感度：HIGH
  保护级别：C3

数据字段：手机号
  分类：contact_info
  敏感度：MEDIUM
  保护级别：C2

数据字段：人脸特征
  分类：biometric_info
  敏感度：CRITICAL
  保护级别：C4
  特殊要求：明示同意、加密存储、严格访问控制

数据字段：购买偏好
  分类：behavioral_data
  敏感度：LOW_MEDIUM
  保护级别：C1

数据字段：IP地址
  分类：network_identifiers
  敏感度：LOW
  保护级别：C1
```

**关键洞察**：
- 生物特征和健康信息属于敏感个人信息，需要最高级别保护
- 不同敏感度的数据应采用不同的保护措施
- 数据分类是实施分级保护的基础

### 示例2：GDPR合规的同意管理系统

**场景**：实现符合GDPR要求的用户同意管理

```python
from datetime import datetime
import json

class ConsentManagementSystem:
    def __init__(self):
        self.consents = {}
    
    def request_consent(self, user_id, purposes, data_types):
        """请求用户同意"""
        consent_request = {
            'request_id': f"CR-{user_id}-{datetime.now().strftime('%Y%m%d%H%M%S')}",
            'user_id': user_id,
            'timestamp': datetime.now().isoformat(),
            'purposes': purposes,  # 处理目的清单
            'data_types': data_types,  # 数据类型清单
            'status': 'PENDING'
        }
        return consent_request
    
    def record_consent(self, user_id, consent_request, granted_purposes):
        """记录用户同意"""
        consent_record = {
            'consent_id': f"C-{user_id}-{datetime.now().strftime('%Y%m%d%H%M%S')}",
            'user_id': user_id,
            'request_id': consent_request['request_id'],
            'granted_at': datetime.now().isoformat(),
            'granted_purposes': granted_purposes,  # 用户同意的目的
            'denied_purposes': list(set(consent_request['purposes']) - set(granted_purposes)),
            'data_types': consent_request['data_types'],
            'consent_method': 'explicit_opt_in',  # 明示同意
            'consent_version': '2.0',  # 隐私政策版本
            'freely_given': True,  # 自愿给予
            'specific': True,  # 具体明确
            'informed': True,  # 充分告知
            'unambiguous': True,  # 明确无疑
            'status': 'ACTIVE',
            'withdrawn_at': None
        }
        self.consents[consent_record['consent_id']] = consent_record
        return consent_record
    
    def withdraw_consent(self, consent_id):
        """撤回同意"""
        if consent_id in self.consents:
            self.consents[consent_id]['status'] = 'WITHDRAWN'
            self.consents[consent_id]['withdrawn_at'] = datetime.now().isoformat()
            return True
        return False
    
    def check_consent(self, user_id, purpose):
        """检查特定目的是否有有效同意"""
        for consent in self.consents.values():
            if (consent['user_id'] == user_id and 
                consent['status'] == 'ACTIVE' and 
                purpose in consent['granted_purposes']):
                return True
        return False
    
    def get_consent_record(self, user_id):
        """用户查询自己的同意记录（数据主体权利）"""
        user_consents = [c for c in self.consents.values() if c['user_id'] == user_id]
        return user_consents

# 使用示例
cms = ConsentManagementSystem()

# 1. 请求用户同意
purposes = [
    '提供核心服务',
    '个性化推荐',
    '营销推广',
    '第三方分析'
]
data_types = ['姓名', '邮箱', '浏览行为', '购买历史']

consent_req = cms.request_consent('USER123', purposes, data_types)
print("同意请求：")
print(json.dumps(consent_req, indent=2, ensure_ascii=False))

# 2. 用户授予部分同意（粒度化同意）
granted = ['提供核心服务', '个性化推荐']  # 用户拒绝营销和第三方分析
consent_record = cms.record_consent('USER123', consent_req, granted)
print("\n同意记录：")
print(json.dumps(consent_record, indent=2, ensure_ascii=False))

# 3. 检查特定目的是否有同意
print(f"\n检查'个性化推荐'是否有同意：{cms.check_consent('USER123', '个性化推荐')}")
print(f"检查'营销推广'是否有同意：{cms.check_consent('USER123', '营销推广')}")

# 4. 用户撤回同意
cms.withdraw_consent(consent_record['consent_id'])
print(f"\n撤回同意后，'个性化推荐'是否仍有同意：{cms.check_consent('USER123', '个性化推荐')}")

# 5. 用户查询同意历史
history = cms.get_consent_record('USER123')
print("\n用户同意历史：")
for record in history:
    print(f"  同意ID：{record['consent_id']}")
    print(f"  状态：{record['status']}")
    print(f"  同意目的：{record['granted_purposes']}")
    print(f"  拒绝目的：{record['denied_purposes']}")
```

**GDPR合规要点**：
- ✅ 明示同意（explicit opt-in）
- ✅ 粒度化同意（用户可选择具体目的）
- ✅ 自由给予、具体、知情、明确
- ✅ 撤回同意机制
- ✅ 同意记录可审计
- ✅ 数据主体访问权（查询同意历史）

### 示例3：数据脱敏和匿名化实现

**场景**：对生产数据进行脱敏，用于开发测试环境

```python
import hashlib
import random
import re

class DataMasking:
    def __init__(self, salt='SECRET_SALT_2025'):
        self.salt = salt
    
    # 1. 替换脱敏（Substitution）
    def mask_name(self, name):
        """姓名脱敏：保留姓，名替换为*"""
        if len(name) <= 1:
            return '*'
        return name[0] + '*' * (len(name) - 1)
    
    # 2. 遮蔽脱敏（Redaction）
    def mask_phone(self, phone):
        """手机号脱敏：保留前3后4位"""
        if len(phone) != 11:
            return '***'
        return phone[:3] + '****' + phone[-4:]
    
    def mask_email(self, email):
        """邮箱脱敏：保留首字母和域名"""
        if '@' not in email:
            return '***'
        local, domain = email.split('@')
        return local[0] + '***@' + domain
    
    def mask_id_card(self, id_card):
        """身份证号脱敏：保留前6后4位"""
        if len(id_card) != 18:
            return '***'
        return id_card[:6] + '********' + id_card[-4:]
    
    # 3. 哈希脱敏（Hashing）- 假名化
    def pseudonymize(self, value):
        """使用加盐哈希进行假名化"""
        return hashlib.sha256(f"{value}{self.salt}".encode()).hexdigest()
    
    # 4. 泛化（Generalization）
    def generalize_age(self, age):
        """年龄泛化为年龄段"""
        if age < 18:
            return '未成年'
        elif age < 30:
            return '18-29岁'
        elif age < 50:
            return '30-49岁'
        else:
            return '50岁以上'
    
    def generalize_address(self, address):
        """地址泛化：只保留省市"""
        # 简化实现：假设地址格式为"省-市-区-详细地址"
        parts = address.split('-')
        if len(parts) >= 2:
            return f"{parts[0]}-{parts[1]}"
        return '***'
    
    # 5. 洗牌（Shuffling）
    def shuffle_dataset(self, data, columns_to_shuffle):
        """对指定列进行洗牌，打乱与其他列的关联"""
        import copy
        shuffled = copy.deepcopy(data)
        for col in columns_to_shuffle:
            values = [row[col] for row in data]
            random.shuffle(values)
            for i, row in enumerate(shuffled):
                row[col] = values[i]
        return shuffled
    
    # 6. K-匿名化
    def k_anonymize(self, data, quasi_identifiers, k=3):
        """简化的k-匿名实现"""
        # 按准标识符分组
        groups = {}
        for record in data:
            key = tuple(record[qi] for qi in quasi_identifiers)
            if key not in groups:
                groups[key] = []
            groups[key].append(record)
        
        # 泛化小于k的组
        anonymized = []
        for group in groups.values():
            if len(group) < k:
                # 泛化处理
                for record in group:
                    for qi in quasi_identifiers:
                        if isinstance(record[qi], int):
                            record[qi] = f"{record[qi]//10*10}-{record[qi]//10*10+9}"
                        else:
                            record[qi] = record[qi][:2] + '***'
            anonymized.extend(group)
        
        return anonymized

# 使用示例
masker = DataMasking()

# 原始数据
original_data = {
    '姓名': '张三',
    '手机号': '13812345678',
    '邮箱': 'zhangsan@example.com',
    '身份证号': '110101199001011234',
    '年龄': 25,
    '地址': '北京市-朝阳区-望京街道-某小区1号楼',
    '用户ID': 'user_12345'
}

# 脱敏处理
masked_data = {
    '姓名': masker.mask_name(original_data['姓名']),
    '手机号': masker.mask_phone(original_data['手机号']),
    '邮箱': masker.mask_email(original_data['邮箱']),
    '身份证号': masker.mask_id_card(original_data['身份证号']),
    '年龄': masker.generalize_age(original_data['年龄']),
    '地址': masker.generalize_address(original_data['地址']),
    '用户假名': masker.pseudonymize(original_data['用户ID'])
}

print("原始数据：")
for k, v in original_data.items():
    print(f"  {k}: {v}")

print("\n脱敏后数据：")
for k, v in masked_data.items():
    print(f"  {k}: {v}")

# K-匿名示例
print("\n\nK-匿名化示例：")
dataset = [
    {'姓名': '张三', '年龄': 25, '邮编': '100000', '疾病': '高血压'},
    {'姓名': '李四', '年龄': 26, '邮编': '100000', '疾病': '糖尿病'},
    {'姓名': '王五', '年龄': 45, '邮编': '200000', '疾病': '心脏病'},  # 唯一，不满足k=3
]

quasi_identifiers = ['年龄', '邮编']
anonymized = masker.k_anonymize(dataset, quasi_identifiers, k=3)

print("原始数据集：")
for record in dataset:
    print(f"  {record}")

print("\nK-匿名化后（k=3）：")
for record in anonymized:
    print(f"  {record}")
```

**脱敏技术对比**：

| 技术       | 可逆性           | 数据可用性 | 隐私保护强度 | 适用场景   |
| ---------- | ---------------- | ---------- | ------------ | ---------- |
| 替换/遮蔽  | 不可逆           | 中等       | 中等         | 展示、报表 |
| 哈希假名化 | 可逆（需映射表） | 高         | 高           | 内部分析   |
| 泛化       | 不可逆           | 中等       | 中等         | 统计分析   |
| K-匿名     | 不可逆           | 较高       | 高           | 数据发布   |
| 洗牌       | 不可逆           | 高（列内） | 中等         | 测试数据   |

### 示例4：数据泄露响应流程模拟

**场景**：模拟数据泄露事件的检测和响应流程

```python
from datetime import datetime, timedelta
import enum

class BreachSeverity(enum.Enum):
    LOW = "低风险"
    MEDIUM = "中等风险"
    HIGH = "高风险"
    CRITICAL = "严重风险"

class DataBreachResponse:
    def __init__(self):
        self.breach_log = []
        self.notification_sent = []
    
    def detect_breach(self, breach_type, affected_records, data_types):
        """阶段1：检测数据泄露"""
        breach_event = {
            'breach_id': f"BR-{datetime.now().strftime('%Y%m%d%H%M%S')}",
            'detected_at': datetime.now(),
            'breach_type': breach_type,  # 如：未授权访问、配置错误、恶意攻击
            'affected_records': affected_records,
            'data_types': data_types,
            'severity': self._assess_severity(affected_records, data_types),
            'status': '已检测'
        }
        self.breach_log.append(breach_event)
        return breach_event
    
    def _assess_severity(self, affected_records, data_types):
        """评估泄露严重程度"""
        sensitive_types = ['身份证号', '银行卡', '生物特征', '健康数据', '密码']
        
        # 包含敏感信息
        has_sensitive = any(dt in sensitive_types for dt in data_types)
        
        # 影响规模
        if affected_records > 10000:
            scale = 'large'
        elif affected_records > 1000:
            scale = 'medium'
        else:
            scale = 'small'
        
        # 综合评估
        if has_sensitive and scale == 'large':
            return BreachSeverity.CRITICAL
        elif has_sensitive or scale == 'large':
            return BreachSeverity.HIGH
        elif scale == 'medium':
            return BreachSeverity.MEDIUM
        else:
            return BreachSeverity.LOW
    
    def contain_breach(self, breach_id):
        """阶段2：遏制泄露"""
        breach = self._find_breach(breach_id)
        if breach:
            # 采取遏制措施
            containment_actions = [
                '隔离受影响系统',
                '停止数据外泄',
                '重置访问凭证',
                '启用额外监控'
            ]
            breach['containment_actions'] = containment_actions
            breach['contained_at'] = datetime.now()
            breach['status'] = '已遏制'
            return True
        return False
    
    def assess_impact(self, breach_id):
        """阶段3：评估影响"""
        breach = self._find_breach(breach_id)
        if breach:
            assessment = {
                'affected_individuals': breach['affected_records'],
                'data_categories': breach['data_types'],
                'potential_harm': self._determine_harm(breach),
                'regulatory_impact': self._check_regulatory_requirements(breach),
                'assessed_at': datetime.now()
            }
            breach['impact_assessment'] = assessment
            breach['status'] = '已评估'
            return assessment
        return None
    
    def _determine_harm(self, breach):
        """确定潜在危害"""
        harms = []
        sensitive_types = {
            '身份证号': '身份盗用风险',
            '银行卡': '财务欺诈风险',
            '生物特征': '永久身份泄露',
            '健康数据': '医疗隐私侵害',
            '密码': '账户被接管风险'
        }
        
        for dt in breach['data_types']:
            if dt in sensitive_types:
                harms.append(sensitive_types[dt])
        
        if not harms:
            harms.append('轻微隐私泄露')
        
        return harms
    
    def _check_regulatory_requirements(self, breach):
        """检查监管通知要求"""
        requirements = {
            'gdpr_notification_required': False,
            'gdpr_deadline': None,
            'ccpa_notification_required': False,
            'pipl_notification_required': False
        }
        
        # GDPR: 影响欧盟居民且存在风险
        if breach['severity'] in [BreachSeverity.HIGH, BreachSeverity.CRITICAL]:
            requirements['gdpr_notification_required'] = True
            requirements['gdpr_deadline'] = datetime.now() + timedelta(hours=72)
            requirements['ccpa_notification_required'] = True
            requirements['pipl_notification_required'] = True
        
        return requirements
    
    def notify_regulator(self, breach_id):
        """阶段4：通知监管机构"""
        breach = self._find_breach(breach_id)
        if breach and breach.get('impact_assessment'):
            assessment = breach['impact_assessment']
            
            # GDPR通知内容
            if assessment['regulatory_impact']['gdpr_notification_required']:
                notification = {
                    'recipient': 'Data Protection Authority',
                    'breach_id': breach_id,
                    'nature_of_breach': breach['breach_type'],
                    'categories_affected': breach['data_types'],
                    'approximate_number': breach['affected_records'],
                    'consequences': assessment['potential_harm'],
                    'measures_taken': breach.get('containment_actions', []),
                    'dpo_contact': 'dpo@company.com',
                    'notified_at': datetime.now()
                }
                
                self.notification_sent.append(notification)
                breach['regulator_notified_at'] = datetime.now()
                breach['status'] = '已通知监管机构'
                
                # 检查是否在72小时内
                time_since_detection = datetime.now() - breach['detected_at']
                if time_since_detection <= timedelta(hours=72):
                    notification['timely'] = True
                else:
                    notification['timely'] = False
                    notification['delay_reason'] = '需要时间评估影响范围'
                
                return notification
        return None
    
    def notify_individuals(self, breach_id):
        """阶段5：通知受影响个人"""
        breach = self._find_breach(breach_id)
        if breach and breach['severity'] in [BreachSeverity.HIGH, BreachSeverity.CRITICAL]:
            assessment = breach['impact_assessment']
            
            individual_notification = {
                'breach_id': breach_id,
                'recipients': f"{breach['affected_records']}名用户",
                'message': {
                    'what_happened': f"发生了{breach['breach_type']}事件",
                    'what_data': f"涉及：{', '.join(breach['data_types'])}",
                    'potential_consequences': assessment['potential_harm'],
                    'what_we_did': breach.get('containment_actions', []),
                    'what_you_should_do': [
                        '更改密码',
                        '监控账户异常',
                        '警惕钓鱼攻击',
                        '考虑启用双因素认证'
                    ],
                    'contact': 'privacy@company.com',
                    'support_available': '免费信用监控服务（1年）'
                },
                'notified_at': datetime.now()
            }
            
            self.notification_sent.append(individual_notification)
            breach['individuals_notified_at'] = datetime.now()
            breach['status'] = '已通知个人'
            
            return individual_notification
        return None
    
    def remediate(self, breach_id):
        """阶段6：修复和改进"""
        breach = self._find_breach(breach_id)
        if breach:
            remediation = {
                'breach_id': breach_id,
                'root_cause': '漏洞分析结果',
                'corrective_actions': [
                    '修复安全漏洞',
                    '加强访问控制',
                    '更新安全策略',
                    '员工再培训'
                ],
                'preventive_measures': [
                    '部署DLP系统',
                    '增强监控能力',
                    '定期安全审计',
                    '渗透测试'
                ],
                'completed_at': datetime.now()
            }
            breach['remediation'] = remediation
            breach['status'] = '已修复'
            return remediation
        return None
    
    def _find_breach(self, breach_id):
        for breach in self.breach_log:
            if breach['breach_id'] == breach_id:
                return breach
        return None
    
    def generate_report(self, breach_id):
        """生成泄露事件报告"""
        breach = self._find_breach(breach_id)
        if breach:
            report = f"""
=== 数据泄露事件报告 ===

事件ID: {breach['breach_id']}
检测时间: {breach['detected_at'].strftime('%Y-%m-%d %H:%M:%S')}
严重程度: {breach['severity'].value}
当前状态: {breach['status']}

影响范围:
  - 受影响记录数: {breach['affected_records']}
  - 数据类型: {', '.join(breach['data_types'])}

时间线:
  - 检测: {breach['detected_at'].strftime('%Y-%m-%d %H:%M:%S')}
  - 遏制: {breach.get('contained_at', 'N/A')}
  - 监管通知: {breach.get('regulator_notified_at', 'N/A')}
  - 个人通知: {breach.get('individuals_notified_at', 'N/A')}

已采取措施:
{chr(10).join('  - ' + action for action in breach.get('containment_actions', []))}

监管合规:
"""
            if breach.get('impact_assessment'):
                reg = breach['impact_assessment']['regulatory_impact']
                report += f"  - GDPR通知要求: {'是' if reg['gdpr_notification_required'] else '否'}\n"
                if reg['gdpr_deadline']:
                    report += f"  - GDPR通知截止: {reg['gdpr_deadline'].strftime('%Y-%m-%d %H:%M:%S')}\n"
            
            return report
        return "未找到该泄露事件"

# 使用示例
drp = DataBreachResponse()

# 模拟数据泄露事件
print("=== 数据泄露响应流程模拟 ===\n")

# 1. 检测泄露
breach = drp.detect_breach(
    breach_type='数据库配置错误导致公开访问',
    affected_records=15000,
    data_types=['姓名', '邮箱', '手机号', '身份证号']
)
print(f"✓ 检测到泄露: {breach['breach_id']}")
print(f"  严重程度: {breach['severity'].value}")
print(f"  影响记录: {breach['affected_records']}条\n")

# 2. 遏制泄露
drp.contain_breach(breach['breach_id'])
print(f"✓ 泄露已遏制")
print(f"  采取措施: {len(breach['containment_actions'])}项\n")

# 3. 评估影响
assessment = drp.assess_impact(breach['breach_id'])
print(f"✓ 影响评估完成")
print(f"  潜在危害: {', '.join(assessment['potential_harm'])}")
print(f"  GDPR通知要求: {assessment['regulatory_impact']['gdpr_notification_required']}\n")

# 4. 通知监管机构
regulator_notice = drp.notify_regulator(breach['breach_id'])
if regulator_notice:
    print(f"✓ 已通知监管机构")
    print(f"  通知时间: {regulator_notice['notified_at'].strftime('%Y-%m-%d %H:%M:%S')}")
    print(f"  是否及时(72h内): {regulator_notice.get('timely', 'N/A')}\n")

# 5. 通知受影响个人
individual_notice = drp.notify_individuals(breach['breach_id'])
if individual_notice:
    print(f"✓ 已通知受影响个人")
    print(f"  通知对象: {individual_notice['recipients']}")
    print(f"  建议行动: {len(individual_notice['message']['what_you_should_do'])}项\n")

# 6. 修复改进
remediation = drp.remediate(breach['breach_id'])
print(f"✓ 修复完成")
print(f"  纠正措施: {len(remediation['corrective_actions'])}项")
print(f"  预防措施: {len(remediation['preventive_measures'])}项\n")

# 生成最终报告
print(drp.generate_report(breach['breach_id']))
```

**关键合规要点**：
- ✅ 及时检测和遏制（24小时内）
- ✅ 72小时内通知监管机构（GDPR）
- ✅ 无不当延迟通知受影响个人
- ✅ 详细记录响应过程
- ✅ 采取补救和预防措施

---

**提示词使用说明:**
本CRISPE提示词可用于AI系统生成关于私有信息保护规则的专业内容，涵盖法律法规、技术措施、管理流程的完整知识体系，适合信息安全合规、系统架构师考试备考、隐私保护体系建设、数据治理等场景。
