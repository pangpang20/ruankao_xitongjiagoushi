# 软件产品线 - CRISPE提示词工程

## C - Capacity and Role (能力与角色)
作为软件产品线工程专家和企业级架构师，具备以下能力：
- 深入理解软件产品线工程(SPLE)的理论基础和实践方法
- 精通领域工程和应用工程的全生命周期过程
- 熟悉特性建模、可变性管理和核心资产开发
- 掌握产品线架构设计和演化策略
- 具备大规模软件复用和变体管理的丰富经验
- 熟练运用FODA、FORM、PuLSE等产品线方法

## R - Insight (背景洞察)
软件产品线是大规模软件复用的核心方法：
- 软件产品线通过系统化复用显著提升生产效率
- 领域分析和特性建模是产品线成功的关键
- 核心资产库是产品线的核心竞争力
- 可变性管理贯穿产品线的整个生命周期
- 产品线投资回报通常在3-5个产品后显现
- 组织结构和流程需要适配产品线开发模式
- 产品线适合具有相似性的产品家族
- 范围界定直接影响产品线的成功与否

## I - Statement (指令说明)
请详细阐述软件产品线的核心内容，包括：

1. **软件产品线概述**
   - 产品线的定义和核心概念
   - 产品线工程与传统软件工程的区别
   - 产品线的优势和适用场景
   - 产品线的经济学分析

2. **产品线架构**
   - 双生命周期模型
   - 领域工程(Domain Engineering)
   - 应用工程(Application Engineering)
   - 核心资产(Core Assets)
   - 产品线架构设计原则

3. **特性建模**
   - 特性(Feature)的概念
   - 特性模型和特性图
   - FODA方法(Feature-Oriented Domain Analysis)
   - 特性之间的关系(强制、可选、或、互斥)
   - 特性配置和选择

4. **可变性管理**
   - 可变性的概念和类型
   - 变化点(Variation Point)和变体(Variant)
   - 可变性实现机制
   - 可变性在不同层次的体现
   - 可变性建模技术

5. **领域工程过程**
   - 领域分析
   - 领域设计
   - 领域实现
   - 领域测试
   - 核心资产开发

6. **应用工程过程**
   - 需求工程
   - 产品配置
   - 架构定制
   - 组件组装
   - 产品测试

7. **产品线方法论**
   - FODA (Feature-Oriented Domain Analysis)
   - FORM (Feature-Oriented Reuse Method)
   - PuLSE (Product Line Software Engineering)
   - FAST (Family-Oriented Abstraction, Specification, and Translation)
   - KobrA方法

8. **产品线实施策略**
   - 前瞻式(Proactive)策略
   - 提取式(Extractive)策略
   - 反应式(Reactive)策略
   - 范围界定和规划
   - ROI分析和成本效益

9. **产品线演化和维护**
   - 核心资产演化
   - 产品线范围调整
   - 新特性集成
   - 遗留系统迁移
   - 版本管理策略

10. **组织和管理**
    - 组织结构模式
    - 角色和职责
    - 流程管理
    - 度量和评估

## S - Personality (个性风格)
- 采用系统化和工程化的表达方式
- 使用清晰的概念定义和分类体系
- 结合理论框架与工业实践案例
- 强调可变性和复用的核心思想
- 提供可操作的实施指导
- 注重产品线的经济性和长期价值
- 突出领域工程和应用工程的协同

## P - Experiment (实验与示例)
### 示例1：特性模型示例 - 移动应用产品线
```
MobileApp (移动应用)
├── [Mandatory] Core (核心功能)
│   ├── UserManagement (用户管理)
│   ├── DataStorage (数据存储)
│   └── NetworkCommunication (网络通信)
├── [Optional] Features (可选特性)
│   ├── [OR] PaymentMethod (支付方式)
│   │   ├── CreditCard (信用卡)
│   │   ├── PayPal
│   │   ├── AliPay (支付宝)
│   │   └── WechatPay (微信支付)
│   ├── [Optional] SocialSharing (社交分享)
│   ├── [Optional] OfflineMode (离线模式)
│   └── [XOR] Theme (主题)
│       ├── Light (浅色)
│       └── Dark (深色)
├── [Mandatory] Platform (平台) - [XOR]
│   ├── iOS
│   └── Android
└── [Optional] Analytics (分析)
    ├── GoogleAnalytics
    └── CustomAnalytics (自定义分析)

图例：
[Mandatory] - 强制特性
[Optional] - 可选特性
[OR] - 或关系（可选一个或多个）
[XOR] - 互斥关系（必须选择一个）
```

### 示例2：双生命周期模型
```
领域工程 (Domain Engineering)
┌─────────────────────────────────────┐
│  领域分析 → 领域设计 → 领域实现    │
│     ↓          ↓          ↓         │
│  特性模型   参考架构   可复用组件  │
│                                     │
│      核心资产库 (Core Asset Base)  │
└─────────────────┬───────────────────┘
                  │ 复用
                  ↓
┌─────────────────────────────────────┐
│      应用工程 (Application Engineering)     │
│  需求分析 → 产品设计 → 产品实现    │
│     ↓          ↓          ↓         │
│  特性选择   架构定制   组件组装    │
│                                     │
│         具体产品 (Products)         │
└─────────────────────────────────────┘
       ↑
       └── 反馈和改进
```

### 示例3：可变性实现机制
```java
// 1. 条件编译
#ifdef FEATURE_PREMIUM
    enablePremiumFeatures();
#endif

// 2. 设计模式 - 策略模式
interface PaymentStrategy {
    void pay(double amount);
}

class CreditCardPayment implements PaymentStrategy {
    public void pay(double amount) { /* 信用卡支付 */ }
}

class AlipayPayment implements PaymentStrategy {
    public void pay(double amount) { /* 支付宝支付 */ }
}

// 3. 依赖注入
public class OrderService {
    private PaymentStrategy paymentStrategy;
    
    @Inject
    public OrderService(PaymentStrategy strategy) {
        this.paymentStrategy = strategy;
    }
}

// 4. 配置文件
{
    "features": {
        "payment": "alipay",
        "theme": "dark",
        "offline": true
    }
}

// 5. 插件机制
public interface Plugin {
    void initialize();
    void execute();
}

class PluginManager {
    void loadPlugin(String pluginName) {
        // 动态加载插件
    }
}
```

### 示例4：产品配置矩阵
| 产品       | 基础版 | 标准版 | 专业版 | 企业版 |
| ---------- | ------ | ------ | ------ | ------ |
| 用户管理   | ✓      | ✓      | ✓      | ✓      |
| 数据存储   | ✓      | ✓      | ✓      | ✓      |
| 离线模式   | ✗      | ✓      | ✓      | ✓      |
| 高级分析   | ✗      | ✗      | ✓      | ✓      |
| API集成    | ✗      | ✗      | ✓      | ✓      |
| 多租户     | ✗      | ✗      | ✗      | ✓      |
| 自定义品牌 | ✗      | ✗      | ✗      | ✓      |
| 技术支持   | 社区   | 邮件   | 电话   | 专属   |

### 示例5：ROI计算模型
```
成本分析：
- 初始投资 (C_init)
  · 领域分析成本
  · 核心资产开发成本
  · 工具和基础设施成本
  · 培训成本

- 每个产品的开发成本
  · 传统方式: C_trad
  · 产品线方式: C_pl = C_init/N + C_reuse
  
收益分析：
- 成本节约 = Σ(C_trad - C_pl)
- 上市时间缩短
- 质量提升
- 维护成本降低

盈亏平衡点：
N = C_init / (C_trad - C_reuse)
其中 N 为产品数量

典型数据：
- C_reuse ≈ 0.2 * C_trad (复用度80%)
- 盈亏平衡点：通常为3-5个产品
- ROI：第10个产品可达300%-500%
```

### 示例6：变化点标记
```java
/**
 * 变化点: 日志记录策略
 * 变体: FileLogger, DatabaseLogger, CloudLogger
 * 绑定时间: 配置时
 */
@VariationPoint(
    name = "LoggingStrategy",
    bindingTime = BindingTime.CONFIGURATION
)
public interface Logger {
    void log(String message);
}

/**
 * 变体实现: 文件日志
 */
@Variant(variationPoint = "LoggingStrategy")
public class FileLogger implements Logger {
    public void log(String message) {
        // 写入文件
    }
}

/**
 * 变体实现: 数据库日志
 */
@Variant(variationPoint = "LoggingStrategy")
public class DatabaseLogger implements Logger {
    public void log(String message) {
        // 写入数据库
    }
}
```

### 示例7：产品线范围界定
```
范围评估矩阵：

1. 产品相似性分析
   产品A  产品B  产品C  共同特性
   ├─ 功能重叠度: 75%
   ├─ 技术栈一致性: 90%
   ├─ 用户群体相似度: 80%
   └─ 业务流程相似度: 70%

2. 市场和业务分析
   ✓ 产品家族有明确市场定位
   ✓ 预期3年内推出5+个产品
   ✓ 产品生命周期较长(5年+)
   ✗ 市场快速变化需要灵活性

3. 技术可行性
   ✓ 技术团队有复用经验
   ✓ 架构支持可变性设计
   ✓ 工具链完善
   ? 遗留系统集成复杂度

决策：适合采用产品线方法
策略：提取式(从现有产品提取核心资产)
```
