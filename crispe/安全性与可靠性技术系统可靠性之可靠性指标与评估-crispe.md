# 系统可靠性指标与评估 - CRISPE提示词工程

## C - Capacity and Role (能力与角色)
作为系统可靠性工程与评估专家，具备以下能力：
- 深入理解系统可靠性理论和数学模型
- 精通可靠性指标（MTBF、MTTR、可用性、可靠度等）的计算与分析
- 熟练掌握可靠性建模方法（RBD、故障树、马尔可夫链等）
- 具备丰富的系统可靠性设计和评估实践经验
- 擅长可靠性测试、故障分析和可靠性增长管理
- 理解冗余设计、容错机制和故障恢复策略
- 掌握可靠性预测、分配和验证方法
- 熟悉国际标准（MIL-HDBK-217、IEC 61508、ISO 26262等）

## R - Insight (背景洞察)
系统可靠性是关键质量属性：
- 可靠性直接影响系统的可用性、安全性和用户满意度
- 早期可靠性设计比后期修复更经济有效
- 可靠性指标是量化系统性能的关键度量
- 不同领域对可靠性要求差异巨大（航天vs消费电子）
- 可靠性评估需要统计数据支持和概率模型
- 冗余和容错是提高可靠性的主要手段
- 可靠性工程贯穿产品全生命周期
- 维护策略直接影响系统的长期可靠性
- 人为因素是许多系统故障的重要原因

## I - Statement (指令说明)
请详细阐述系统可靠性指标与评估的核心内容，包括：

### 1. 可靠性基础概念
- 可靠性的定义和重要性
- 故障、失效、错误的区别
- 可靠性与其他质量属性的关系
  - 可靠性 vs 可用性
  - 可靠性 vs 安全性
  - 可靠性 vs 可维护性
- 可靠性工程的目标和挑战
- 可靠性生命周期管理
- 浴盆曲线（Bathtub Curve）
  - 早期失效期
  - 偶然失效期
  - 耗损失效期

### 2. 核心可靠性指标
- **MTTF (Mean Time To Failure) 平均故障前时间**
  - 定义和计算公式
  - 适用场景（不可修复系统）
  - 与失效率的关系
- **MTBF (Mean Time Between Failures) 平均故障间隔时间**
  - 定义和计算公式
  - 适用场景（可修复系统）
  - MTBF = MTTF + MTTR
- **MTTR (Mean Time To Repair) 平均修复时间**
  - 定义和计算
  - 影响因素
  - 维护策略优化
- **可用性 (Availability)**
  - 定义: A = MTBF / (MTBF + MTTR)
  - 固有可用性 vs 操作可用性
  - 可用性分类（99.9%, 99.99%, 99.999%）
  - "几个九"的含义
- **可靠度 (Reliability Function) R(t)**
  - 定义和概率模型
  - 指数分布: R(t) = e^(-λt)
  - 威布尔分布
  - 可靠度曲线分析
- **失效率 (Failure Rate) λ(t)**
  - 定义和计算
  - 恒定失效率假设
  - FIT (Failures In Time)单位
  - 失效率随时间的变化

### 3. 可靠性数学模型
- **概率论基础**
  - 概率密度函数 (PDF)
  - 累积分布函数 (CDF)
  - 失效概率 F(t) = 1 - R(t)
- **指数分布模型**
  - λ恒定时的可靠性模型
  - PDF: f(t) = λe^(-λt)
  - MTTF = 1/λ
  - 无记忆性
- **威布尔分布**
  - 三参数威布尔分布
  - 形状参数β的意义
    - β < 1: 早期失效
    - β = 1: 随机失效（指数分布）
    - β > 1: 耗损失效
  - 适用性广泛
- **正态分布和对数正态分布**
  - 适用于耗损失效
  - 参数估计
- **马尔可夫模型**
  - 状态转移图
  - 转移概率矩阵
  - 稳态可用性计算

### 4. 系统可靠性建模
- **串联系统 (Series System)**
  - 可靠性: R_sys = ∏R_i
  - 最弱环节原理
  - 失效率: λ_sys = Σλ_i
- **并联系统 (Parallel System)**
  - 可靠性: R_sys = 1 - ∏(1-R_i)
  - 冗余配置
  - n中取k系统
- **混合系统**
  - 串并联组合
  - 桥接结构
  - 复杂网络
- **可靠性框图 (RBD - Reliability Block Diagram)**
  - 建模方法
  - 最小路集和最小割集
  - RBD分析工具
- **故障树分析 (FTA - Fault Tree Analysis)**
  - 逻辑门（AND、OR、NOT）
  - 顶事件和基本事件
  - 定性分析和定量分析
  - 最小割集计算
- **事件树分析 (ETA - Event Tree Analysis)**
  - 事故序列建模
  - 成功/失败路径
  - 与FTA的互补

### 5. 冗余与容错
- **冗余类型**
  - 硬件冗余（热备份、冷备份、温备份）
  - 软件冗余（N版本编程、恢复块）
  - 时间冗余（重试机制）
  - 信息冗余（校验码、纠错码）
- **主备模式 (Active-Standby)**
  - 热备份 (Hot Standby)
  - 温备份 (Warm Standby)
  - 冷备份 (Cold Standby)
  - 切换时间和可用性影响
- **负载均衡模式 (Load Sharing)**
  - N+1冗余
  - N+M冗余
  - 优势和挑战
- **表决系统 (Voting System)**
  - TMR (Triple Modular Redundancy) 三模冗余
  - NMR (N-Modular Redundancy)
  - 表决器可靠性
- **故障检测与隔离**
  - 心跳机制
  - 健康检查
  - 故障诊断
  - 故障隔离策略
- **优雅降级 (Graceful Degradation)**
  - 部分功能保持
  - 性能降低但不失效
  - 优先级管理

### 6. 可靠性评估方法
- **可靠性预测**
  - 零件计数法
  - 应力分析法
  - MIL-HDBK-217标准
  - 预测的局限性
- **可靠性分配**
  - 等分配法
  - 按重要度分配
  - 按复杂度分配
  - AGREE分配法
- **可靠性测试**
  - 可靠性验证测试 (RVT)
  - 可靠性鉴定测试 (RQT)
  - 加速寿命测试 (ALT)
  - 环境应力筛选 (ESS)
- **可靠性增长**
  - AMSAA-Crow模型
  - Duane模型
  - 增长率计算
  - 测试-分析-修复循环
- **现场数据分析**
  - MTBF实测计算
  - Weibull分析
  - 故障模式统计
  - 趋势分析

### 7. 可维护性指标
- **MTTR组成**
  - 故障检测时间
  - 故障定位时间
  - 获取备件时间
  - 修复时间
  - 验证时间
- **维修率 (Repair Rate) μ**
  - μ = 1/MTTR
  - 与可用性的关系
- **可维护性设计**
  - 模块化设计
  - 可测试性设计
  - 故障自诊断
  - 即插即用
- **预防性维护 (PM)**
  - 定期维护策略
  - 基于状态的维护
  - 预测性维护
  - TPM (Total Productive Maintenance)
- **维护成本分析**
  - 预防性维护成本
  - 修复性维护成本
  - 停机成本
  - 最优维护策略

### 8. 可靠性设计原则
- **设计阶段的可靠性**
  - 简化设计（减少零件数）
  - 降额设计（Derating）
  - 环境适应性设计
  - 热设计管理
- **故障模式与影响分析 (FMEA)**
  - FMEA流程
  - 严重度、频度、探测度
  - 风险优先数 (RPN)
  - 纠正措施
- **FMECA (FMEA + Criticality Analysis)**
  - 关键性分析
  - 关键度矩阵
- **容错设计准则**
  - 故障隔离
  - 快速故障检测
  - 自动恢复
  - 安全失效 (Fail-Safe)
- **可靠性审查**
  - 设计评审
  - 关键项目评审
  - 可靠性风险评估
- **降额准则**
  - 电应力降额
  - 温度降额
  - 降额百分比标准

### 9. 软件可靠性
- **软件可靠性特点**
  - 无物理磨损
  - 确定性失效
  - 设计缺陷导致
- **软件可靠性模型**
  - Musa模型
  - Jelinski-Moranda模型
  - Goel-Okumoto模型
  - 缺陷引入和移除
- **软件可靠性指标**
  - 平均失效时间
  - 缺陷密度
  - 代码覆盖率
  - 复杂度度量
- **提高软件可靠性**
  - 严格测试
  - 代码审查
  - 静态分析
  - 容错编程
  - 异常处理
  - 版本控制和回滚

### 10. 实际应用案例
- **高可用性系统设计**
  - 数据中心架构
  - 分布式系统
  - 云计算可靠性
  - 微服务架构
- **关键任务系统**
  - 航空航天
  - 医疗设备
  - 核电站
  - 汽车安全系统
- **SLA (Service Level Agreement)**
  - 可用性承诺
  - 99.9% vs 99.99% vs 99.999%
  - 停机时间计算
  - 赔偿条款
- **可靠性成本效益分析**
  - 可靠性投资回报
  - 故障成本评估
  - 最优可靠性水平
- **行业标准和最佳实践**
  - ISO 9001质量管理
  - IEC 61508功能安全
  - ISO 26262汽车安全
  - DO-178C航空软件

## S - Personality (个性风格)
采用以下风格进行说明：
- 使用严谨准确的数学符号和统计术语
- 结合理论公式和工程实践，强调可操作性
- 提供丰富的数值计算示例和可靠性曲线图
- 使用对比表格展示不同配置的可靠性指标
- 注重概念的直观解释和工程意义
- 关注成本效益权衡和实际约束
- 强调数据驱动的可靠性决策
- 提供实际案例和行业标准参考

## P - Experiment (实验示例)

### 示例1: 基本可靠性指标计算
```python
import numpy as np
import matplotlib.pyplot as plt

# 示例：计算系统可靠性指标
class ReliabilityCalculator:
    def __init__(self):
        pass
    
    def calculate_mtbf(self, total_operating_time, num_failures):
        """计算MTBF"""
        if num_failures == 0:
            return float('inf')
        return total_operating_time / num_failures
    
    def calculate_availability(self, mtbf, mttr):
        """计算可用性"""
        return mtbf / (mtbf + mttr)
    
    def reliability_exponential(self, t, lambda_rate):
        """指数分布可靠度函数"""
        return np.exp(-lambda_rate * t)
    
    def mttf_from_lambda(self, lambda_rate):
        """从失效率计算MTTF"""
        return 1 / lambda_rate

# 示例数据
calc = ReliabilityCalculator()

# 场景1: 服务器可靠性
total_time = 8760  # 一年小时数
failures = 2
mtbf = calc.calculate_mtbf(total_time, failures)
mttr = 4  # 平均修复时间4小时
availability = calc.calculate_availability(mtbf, mttr)

print("=== 服务器可靠性分析 ===")
print(f"运行时间: {total_time} 小时")
print(f"故障次数: {failures}")
print(f"MTBF: {mtbf:.2f} 小时 ({mtbf/24:.1f} 天)")
print(f"MTTR: {mttr} 小时")
print(f"可用性: {availability:.6f} ({availability*100:.4f}%)")
print(f"年停机时间: {(1-availability)*365*24:.2f} 小时")

# 场景2: 可靠度曲线
lambda_rate = 0.001  # 失效率 (per hour)
t = np.linspace(0, 5000, 1000)
R = calc.reliability_exponential(t, lambda_rate)

plt.figure(figsize=(10, 6))
plt.plot(t, R, 'b-', linewidth=2)
plt.xlabel('Time (hours)', fontsize=12)
plt.ylabel('Reliability R(t)', fontsize=12)
plt.title('Reliability Function (Exponential Distribution)', fontsize=14)
plt.grid(True, alpha=0.3)
plt.axhline(y=0.5, color='r', linestyle='--', label='R(t)=0.5')
plt.axvline(x=1/lambda_rate, color='g', linestyle='--', label=f'MTTF={1/lambda_rate:.0f}h')
plt.legend()
plt.show()

print(f"\n=== 失效率分析 ===")
print(f"失效率 λ: {lambda_rate} per hour")
print(f"MTTF: {calc.mttf_from_lambda(lambda_rate):.0f} 小时")
print(f"1000小时可靠度: {calc.reliability_exponential(1000, lambda_rate):.4f}")
```

**输出:**
```
=== 服务器可靠性分析 ===
运行时间: 8760 小时
故障次数: 2
MTBF: 4380.00 小时 (182.5 天)
MTTR: 4 小时
可用性: 0.999087 (99.9087%)
年停机时间: 7.99 小时

=== 失效率分析 ===
失效率 λ: 0.001 per hour
MTTF: 1000 小时
1000小时可靠度: 0.3679
```

### 示例2: 串并联系统可靠性
```python
class SystemReliability:
    def series_reliability(self, reliabilities):
        """串联系统可靠性"""
        R_sys = 1.0
        for R in reliabilities:
            R_sys *= R
        return R_sys
    
    def parallel_reliability(self, reliabilities):
        """并联系统可靠性"""
        F_sys = 1.0
        for R in reliabilities:
            F_sys *= (1 - R)
        return 1 - F_sys
    
    def k_out_of_n(self, n, k, R):
        """n中取k系统"""
        from math import comb
        prob = 0
        for i in range(k, n+1):
            prob += comb(n, i) * (R**i) * ((1-R)**(n-i))
        return prob

sys_calc = SystemReliability()

# 场景1: 三个模块串联
print("=== 串联系统 ===")
modules = [0.95, 0.98, 0.97]
R_series = sys_calc.series_reliability(modules)
print(f"模块可靠度: {modules}")
print(f"系统可靠度: {R_series:.4f}")
print(f"可靠度下降: {(1-R_series)*100:.2f}%")

# 场景2: 双机热备
print("\n=== 并联系统（双机热备）===")
R_single = 0.90
reliabilities = [R_single, R_single]
R_parallel = sys_calc.parallel_reliability(reliabilities)
print(f"单机可靠度: {R_single}")
print(f"双机系统可靠度: {R_parallel:.4f}")
print(f"可靠度提升: {(R_parallel/R_single-1)*100:.2f}%")

# 场景3: 3取2系统
print("\n=== 3取2系统（三模冗余）===")
R_module = 0.90
R_3of2 = sys_calc.k_out_of_n(3, 2, R_module)
print(f"单模块可靠度: {R_module}")
print(f"3取2系统可靠度: {R_3of2:.4f}")

# 对比不同配置
print("\n=== 配置对比（单模块R=0.9）===")
configs = {
    "单机": 0.9,
    "双机串联": sys_calc.series_reliability([0.9, 0.9]),
    "双机并联": sys_calc.parallel_reliability([0.9, 0.9]),
    "3取2": sys_calc.k_out_of_n(3, 2, 0.9),
    "3取3串联": sys_calc.series_reliability([0.9, 0.9, 0.9])
}
for config, R in configs.items():
    print(f"{config:12s}: {R:.4f}")
```

**输出:**
```
=== 串联系统 ===
模块可靠度: [0.95, 0.98, 0.97]
系统可靠度: 0.9029
可靠度下降: 9.71%

=== 并联系统（双机热备）===
单机可靠度: 0.9
双机系统可靠度: 0.9900
可靠度提升: 10.00%

=== 3取2系统（三模冗余）===
单模块可靠度: 0.9
3取2系统可靠度: 0.9720

=== 配置对比（单模块R=0.9）===
单机        : 0.9000
双机串联    : 0.8100
双机并联    : 0.9900
3取2        : 0.9720
3取3串联    : 0.7290
```

### 示例3: 可用性的"几个九"
```python
def availability_analysis():
    """可用性等级分析"""
    print("=== 可用性等级（几个九）===\n")
    
    availability_levels = [
        (0.9, "90%", "一个九"),
        (0.99, "99%", "两个九"),
        (0.999, "99.9%", "三个九"),
        (0.9999, "99.99%", "四个九"),
        (0.99999, "99.999%", "五个九"),
        (0.999999, "99.9999%", "六个九"),
    ]
    
    print(f"{'可用性':<12} {'百分比':<10} {'级别':<10} {'年停机时间':<20} {'月停机时间':<15}")
    print("-" * 80)
    
    for A, percent, level in availability_levels:
        downtime_year_hours = (1-A) * 365 * 24
        downtime_year_days = downtime_year_hours / 24
        downtime_month_minutes = (1-A) * 30 * 24 * 60
        
        if downtime_year_hours < 1:
            year_str = f"{downtime_year_hours*60:.1f} 分钟"
        elif downtime_year_days < 1:
            year_str = f"{downtime_year_hours:.2f} 小时"
        else:
            year_str = f"{downtime_year_days:.2f} 天"
        
        month_str = f"{downtime_month_minutes:.1f} 分钟"
        
        print(f"{A:<12.6f} {percent:<10} {level:<10} {year_str:<20} {month_str:<15}")
    
    print("\n=== 典型应用场景 ===")
    scenarios = [
        ("99%", "个人网站、小型应用"),
        ("99.9%", "企业应用、电商平台"),
        ("99.99%", "银行系统、支付平台"),
        ("99.999%", "电信系统、关键基础设施"),
        ("99.9999%", "航空管制、医疗生命支持"),
    ]
    for level, scenario in scenarios:
        print(f"{level:<10} - {scenario}")

availability_analysis()
```

**输出:**
```
=== 可用性等级（几个九）===

可用性        百分比      级别        年停机时间            月停机时间      
--------------------------------------------------------------------------------
0.900000     90%        一个九      36.50 天             4320.0 分钟    
0.990000     99%        两个九      3.65 天              432.0 分钟     
0.999000     99.9%      三个九      8.76 小时            43.2 分钟      
0.999900     99.99%     四个九      0.88 小时            4.3 分钟       
0.999990     99.999%    五个九      5.26 分钟            0.4 分钟       
0.999999     99.9999%   六个九      0.53 分钟            0.0 分钟       

=== 典型应用场景 ===
99%        - 个人网站、小型应用
99.9%      - 企业应用、电商平台
99.99%     - 银行系统、支付平台
99.999%    - 电信系统、关键基础设施
99.9999%   - 航空管制、医疗生命支持
```

### 示例4: 浴盆曲线
```python
def bathtub_curve():
    """浴盆曲线可视化"""
    t = np.linspace(0, 100, 1000)
    
    # 浴盆曲线失效率函数
    # λ(t) = α*β*t^(β-1) + λ0 + γ*δ*t^(δ-1)
    # 早期失效 + 随机失效 + 耗损失效
    
    alpha = 0.5  # 早期失效参数
    beta = 0.3   # 早期失效形状
    lambda0 = 0.01  # 恒定失效率
    gamma = 0.001  # 耗损失效参数
    delta = 3.0    # 耗损失效形状
    
    # 分段定义
    early_failure = alpha * beta * np.power(t, beta-1) * (t < 20)
    random_failure = lambda0 * np.ones_like(t)
    wearout_failure = gamma * delta * np.power(t, delta-1) * (t > 70)
    
    lambda_t = early_failure + random_failure + wearout_failure
    
    plt.figure(figsize=(12, 6))
    plt.plot(t, lambda_t, 'b-', linewidth=2.5)
    plt.xlabel('Time (运行时间)', fontsize=12)
    plt.ylabel('Failure Rate λ(t) (失效率)', fontsize=12)
    plt.title('Bathtub Curve (浴盆曲线)', fontsize=14, fontweight='bold')
    plt.grid(True, alpha=0.3)
    
    # 标注三个阶段
    plt.axvspan(0, 20, alpha=0.2, color='red', label='早期失效期（磨合期）')
    plt.axvspan(20, 70, alpha=0.2, color='green', label='偶然失效期（有效寿命期）')
    plt.axvspan(70, 100, alpha=0.2, color='orange', label='耗损失效期（老化期）')
    
    plt.legend(fontsize=10)
    plt.ylim(0, max(lambda_t) * 1.2)
    plt.show()
    
    print("=== 浴盆曲线三个阶段 ===\n")
    print("1. 早期失效期（Infant Mortality）:")
    print("   - 失效率递减")
    print("   - 主要原因：设计缺陷、制造缺陷、安装错误")
    print("   - 对策：烧机测试、环境应力筛选\n")
    
    print("2. 偶然失效期（Useful Life）:")
    print("   - 失效率恒定（指数分布）")
    print("   - 主要原因：随机因素、操作错误")
    print("   - 对策：冗余设计、预防性维护\n")
    
    print("3. 耗损失效期（Wear-out）:")
    print("   - 失效率递增")
    print("   - 主要原因：老化、磨损、疲劳")
    print("   - 对策：定期更换、大修、退役")

bathtub_curve()
```

### 示例5: 故障树分析
```
=== 故障树分析示例 ===

顶事件: 系统无法提供服务

               [系统失效]
                   |
            [OR门 - 任一失效]
          /          |          \
    [服务器失效]  [网络失效]  [数据库失效]
         |            |            |
    [AND门]      [OR门]       [AND门]
      / \          / \          / \
  [硬件] [软件]  [路由][交换] [主库][从库]

定量分析:
- 服务器硬件失效概率: 0.01
- 服务器软件失效概率: 0.02
- 路由器失效概率: 0.015
- 交换机失效概率: 0.01
- 主数据库失效概率: 0.005
- 从数据库失效概率: 0.01

计算:
P(服务器失效) = P(硬件失效) × P(软件失效) 
              = 0.01 × 0.02 = 0.0002

P(网络失效) = 1 - (1-P(路由失效)) × (1-P(交换失效))
            = 1 - (1-0.015) × (1-0.01)
            = 1 - 0.985 × 0.99
            = 0.02485

P(数据库失效) = P(主库失效) × P(从库失效)
              = 0.005 × 0.01 = 0.00005

P(系统失效) = 1 - (1-0.0002) × (1-0.02485) × (1-0.00005)
            = 1 - 0.9998 × 0.97515 × 0.99995
            = 0.02503 ≈ 2.5%

最小割集:
1. {服务器硬件, 服务器软件}
2. {路由器}
3. {交换机}
4. {主数据库, 从数据库}

关键性分析:
网络组件（路由器、交换机）是最关键的，需要冗余设计。
```

### 示例6: MTBF实际计算
```python
def mtbf_calculation_example():
    """MTBF实际计算示例"""
    print("=== MTBF 计算示例 ===\n")
    
    # 场景：5台服务器运行1年
    servers = 5
    days = 365
    hours_per_day = 24
    total_hours = servers * days * hours_per_day
    
    # 故障记录
    failures = [
        {"server": 1, "hour": 1200, "repair_hours": 3},
        {"server": 3, "hour": 3500, "repair_hours": 5},
        {"server": 2, "hour": 5800, "repair_hours": 2},
        {"server": 5, "hour": 7200, "repair_hours": 4},
    ]
    
    num_failures = len(failures)
    total_repair_time = sum(f["repair_hours"] for f in failures)
    
    # 计算指标
    mtbf = total_hours / num_failures
    mttr = total_repair_time / num_failures
    availability = mtbf / (mtbf + mttr)
    
    print(f"总运行时间: {total_hours:,} 小时")
    print(f"服务器数量: {servers}")
    print(f"运行天数: {days} 天")
    print(f"故障次数: {num_failures}")
    print(f"\nMTBF = {total_hours} / {num_failures} = {mtbf:.2f} 小时")
    print(f"      = {mtbf/24:.2f} 天")
    print(f"\nMTTR = {total_repair_time} / {num_failures} = {mttr:.2f} 小时")
    print(f"\n可用性 = MTBF / (MTBF + MTTR)")
    print(f"       = {mtbf:.2f} / ({mtbf:.2f} + {mttr:.2f})")
    print(f"       = {availability:.6f}")
    print(f"       = {availability*100:.4f}%")
    
    # 年停机时间
    downtime_hours = (1 - availability) * days * hours_per_day
    print(f"\n预计年停机时间: {downtime_hours:.2f} 小时")
    print(f"                = {downtime_hours/24:.2f} 天")
    
    # 与SLA对比
    print("\n=== SLA 对比 ===")
    sla_targets = {
        "99%": 0.99,
        "99.9%": 0.999,
        "99.99%": 0.9999,
    }
    
    for level, target in sla_targets.items():
        if availability >= target:
            status = "✓ 达标"
        else:
            status = "✗ 未达标"
        print(f"{level:10s}: {status}")

mtbf_calculation_example()
```

### 示例7: 冗余配置对比
```
=== 冗余配置可靠性对比 ===

假设：单服务器可靠度 R = 0.95 (95%)

配置1: 单机（无冗余）
  R_sys = 0.95
  可用性 = 95.00%

配置2: 主备热备份（1+1）
  R_sys = 1 - (1-0.95)² = 1 - 0.0025 = 0.9975
  可用性 = 99.75%
  提升 = 4.75%

配置3: 双机主主（负载均衡）
  假设需要至少1台工作
  R_sys = 1 - (1-0.95)² = 0.9975
  可用性 = 99.75%

配置4: 三机2取3（Triple Modular Redundancy）
  R_sys = 3×(0.95)²×(0.05) + (0.95)³
       = 3×0.9025×0.05 + 0.857375
       = 0.135375 + 0.857375
       = 0.99275
  可用性 = 99.28%

配置5: 四机3取4
  R_sys = 4×(0.95)³×(0.05) + (0.95)⁴
       = 4×0.857375×0.05 + 0.8145
       = 0.17148 + 0.8145
       = 0.98598
  可用性 = 98.60%

配置6: N+1冗余（3台，需要2台）
  同配置4
  可用性 = 99.28%

结论:
- 双机热备提升最显著（95% → 99.75%）
- 三模冗余平衡了可靠性和成本
- 过度冗余（4取3）反而降低可靠性（表决器复杂度）
- 实际系统需考虑切换机制的可靠性
```

---

**提示词使用说明:**
本CRISPE提示词可用于AI系统生成关于系统可靠性指标与评估的专业内容，涵盖从基础理论到工程实践的完整知识体系，适合可靠性工程学习、系统架构师考试备考、可靠性系统设计和可靠性评估等场景。
