# Security Protocols: SSL/TLS, PGP, IPSec - Comprehensive Technical Documentation

# 安全性与可靠性技术信息安全与保密之安全协议SSL,PGP,IPSec - 完整技术文档

---

## Table of Contents | 目录

1. [Introduction | 概述](#introduction--概述)
2. [Information Security Fundamentals | 信息安全基础](#information-security-fundamentals--信息安全基础)
3. [Cryptography Fundamentals | 密码学基础](#cryptography-fundamentals--密码学基础)
4. [SSL/TLS Protocol | SSL/TLS协议](#ssltls-protocol--ssltls协议)
5. [PGP Protocol | PGP协议](#pgp-protocol--pgp协议)
6. [IPSec Protocol | IPSec协议](#ipsec-protocol--ipsec协议)
7. [Protocol Comparison | 协议对比](#protocol-comparison--协议对比)
8. [Security Attacks and Defenses | 安全攻击与防护](#security-attacks-and-defenses--安全攻击与防护)
9. [Exam Focus Points | 考试要点](#exam-focus-points--考试要点)

---

## Introduction | 概述

### What are Security Protocols? | 什么是安全协议?

**English:**

**Security Protocols** are cryptographic protocols designed to provide secure communication over insecure networks. They use cryptographic techniques to ensure confidentiality, integrity, authentication, and non-repudiation of data transmitted between parties.

**Key Security Protocols | 关键安全协议**:

1. **SSL/TLS (Secure Sockets Layer / Transport Layer Security)**
   - **Layer**: Between Application and Transport layers
   - **Purpose**: Secure web communications (HTTPS)
   - **Use Cases**: Web browsers, email, instant messaging

2. **PGP (Pretty Good Privacy)**
   - **Layer**: Application layer
   - **Purpose**: Email encryption and digital signatures
   - **Use Cases**: Secure email, file encryption

3. **IPSec (Internet Protocol Security)**
   - **Layer**: Network layer (IP layer)
   - **Purpose**: VPN and site-to-site encryption
   - **Use Cases**: Corporate VPNs, secure tunnels

**Why Security Protocols Matter | 安全协议的重要性**:

**For Data Protection | 对数据保护**:
- **Encryption**: Protect sensitive data from eavesdropping
- **Integrity**: Detect tampering and modifications
- **Authentication**: Verify identity of communicating parties

**For Business | 对业务**:
- **Compliance**: Meet regulatory requirements (GDPR, HIPAA, PCI-DSS)
- **Trust**: Build customer confidence
- **Risk Mitigation**: Prevent data breaches and financial losses

**For System Architects Exam | 对系统架构设计师考试**:
- **Core Topic**: Security protocols account for 10-15% of exam content
- **Case Analysis**: Protocol selection, VPN design, HTTPS deployment
- **Technical Depth**: Understanding of handshake processes, key exchange, attack vectors

**Protocol Evolution | 协议演进**:
```
1990s:      SSL 2.0, SSL 3.0 (Netscape)
            PGP 1.0 (Phil Zimmermann)
            
Late 1990s: TLS 1.0 (IETF standard)
            IPSec standardization (RFC 2401-2412)
            
2000s:      TLS 1.1, TLS 1.2
            OpenPGP standard (RFC 4880)
            IKEv2 (improved key exchange)
            
2018:       TLS 1.3 (major overhaul)
            - Faster handshake
            - Stronger security
            - Removed legacy ciphers
```

**中文:**

**安全协议**是设计用于在不安全网络上提供安全通信的密码协议。它们使用密码技术确保通信双方之间传输数据的机密性、完整性、认证性和不可否认性。

**三大安全协议**: SSL/TLS（Web安全）、PGP（邮件加密）、IPSec（网络层VPN）

---

## Information Security Fundamentals | 信息安全基础

### 1.1 CIA Triad | CIA三元组

**English:**

The **CIA Triad** is the foundational model for information security, consisting of three core principles that guide security policies and mechanisms.

**1. Confidentiality | 机密性**

**Definition | 定义**: Ensuring that information is accessible only to authorized individuals or systems.

**Mechanisms | 机制**:
```
- Encryption (加密)
  - Symmetric: AES, 3DES
  - Asymmetric: RSA, ECC
  
- Access Control (访问控制)
  - Authentication: Username/password, biometrics
  - Authorization: Role-Based Access Control (RBAC)
  - Principle of Least Privilege
  
- Information Hiding (信息隐藏)
  - Steganography
  - Data masking
```

**Threats | 威胁**:
```
✗ Eavesdropping (窃听): Passive interception of data
✗ Shoulder Surfing (肩窥): Visual observation
✗ Social Engineering (社会工程学): Manipulating people
✗ Data Leakage (数据泄露): Unauthorized disclosure
```

**2. Integrity | 完整性**

**Definition | 定义**: Ensuring that information is accurate, complete, and has not been tampered with.

**Mechanisms | 机制**:
```
- Hash Functions (哈希函数)
  - MD5 (deprecated), SHA-1 (deprecated)
  - SHA-256, SHA-3
  
- Digital Signatures (数字签名)
  - RSA signature
  - ECDSA (Elliptic Curve Digital Signature Algorithm)
  
- Message Authentication Code (MAC)
  - HMAC (Hash-based MAC)
  - CBC-MAC
  
- Checksums (校验和)
  - CRC (Cyclic Redundancy Check)
```

**Threats | 威胁**:
```
✗ Data Modification (数据篡改): Altering data in transit
✗ Man-in-the-Middle (中间人攻击): Intercepting and modifying
✗ Replay Attacks (重放攻击): Resending valid data
✗ Malware (恶意软件): Trojans, viruses
```

**3. Availability | 可用性**

**Definition | 定义**: Ensuring that information and systems are accessible and functional when needed.

**Mechanisms | 机制**:
```
- Redundancy (冗余)
  - Hardware redundancy (RAID, clustering)
  - Geographic redundancy (multi-datacenter)
  
- Backup and Recovery (备份与恢复)
  - Regular backups (full, incremental, differential)
  - Disaster recovery plans
  
- DDoS Protection (DDoS防护)
  - Rate limiting
  - Traffic filtering
  - CDN (Content Delivery Network)
  
- Fault Tolerance (容错)
  - Failover mechanisms
  - Load balancing
```

**Threats | 威胁**:
```
✗ Denial of Service (DoS) (拒绝服务): Overwhelming resources
✗ Distributed DoS (DDoS) (分布式拒绝服务): Multiple sources
✗ Hardware Failures (硬件故障): Disk crashes, power outages
✗ Natural Disasters (自然灾害): Floods, earthquakes
```

**Extended Security Properties | 扩展安全属性**:

**4. Authentication | 认证**

**Definition | 定义**: Verifying the identity of users, devices, or systems.

**Types | 类型**:
```
- Something You Know (知识因素): Password, PIN
- Something You Have (持有因素): Smart card, token
- Something You Are (生物因素): Fingerprint, facial recognition
- Multi-Factor Authentication (MFA) (多因素认证): Combination of above
```

**5. Non-Repudiation | 不可否认性**

**Definition | 定义**: Preventing a party from denying the authenticity of their signature or the sending of a message.

**Mechanisms | 机制**:
```
- Digital Signatures (数字签名): Cryptographic proof
- Audit Logs (审计日志): Timestamped records
- Trusted Third Party (可信第三方): Notarization services
```

**6. Access Control | 访问控制**

**Definition | 定义**: Restricting access to resources based on policies.

**Models | 模型**:
```
- Discretionary Access Control (DAC) (自主访问控制)
  - Owner decides permissions
  
- Mandatory Access Control (MAC) (强制访问控制)
  - System enforces security labels
  
- Role-Based Access Control (RBAC) (基于角色的访问控制)
  - Permissions assigned to roles
  
- Attribute-Based Access Control (ABAC) (基于属性的访问控制)
  - Policies based on attributes (user, resource, environment)
```

**Security Tradeoffs | 安全权衡**:

```
Confidentiality vs. Availability
- Strong encryption may impact performance/availability
- Example: Encrypted backups slower to restore

Integrity vs. Performance
- Digital signatures add overhead
- Hash verification takes time

Security vs. Usability
- Complex passwords harder to remember
- MFA adds friction to user experience
```

**中文:**

**CIA三元组**是信息安全的基础模型，由三个核心原则组成：

1. **机密性（Confidentiality）**: 确保信息仅对授权个人或系统可访问
2. **完整性（Integrity）**: 确保信息准确、完整且未被篡改
3. **可用性（Availability）**: 确保信息和系统在需要时可访问和可用

**扩展属性**: 认证、不可否认性、访问控制

**[Exam Focus | 考试重点]**: 
- Understand CIA triad and identify appropriate mechanisms for each
- Recognize threats to confidentiality, integrity, availability
- Differentiate authentication vs. authorization vs. non-repudiation
- Compare access control models (DAC, MAC, RBAC, ABAC)

### 1.2 Threat Models and Attack Types | 威胁模型与攻击类型

**English:**

**Passive Attacks | 被动攻击**

**Characteristics | 特征**:
- Attacker observes but does not modify data
- Difficult to detect
- Violates confidentiality

**Types | 类型**:

**1. Eavesdropping (Sniffing) | 窃听（嗅探）**
```
Attacker              Network              Victims
   │                     │                   │
   │  ┌─────────────────┼──────────────────┐│
   │  │  Packet Capture │                  ││
   │  │  (Wireshark)    │                  ││
   │  └─────────────────┼──────────────────┘│
   │                     │                   │
   ▼                     ▼                   ▼
Captured                Unencrypted         Communication
Packets                 Traffic             Continues

Defense: Encryption (SSL/TLS, IPSec)
防御: 加密
```

**2. Traffic Analysis | 流量分析**
```
Even with encryption, attacker can infer:
- Communication patterns (who talks to whom)
- Message sizes and timing
- Network topology

Defense: Padding, dummy traffic, VPN
防御: 填充、虚拟流量、VPN
```

**Active Attacks | 主动攻击**

**Characteristics | 特征**:
- Attacker modifies or disrupts data
- Easier to detect but harder to prevent
- Violates integrity and availability

**Types | 类型**:

**1. Man-in-the-Middle (MitM) | 中间人攻击**
```
Client                Attacker              Server
  │                      │                    │
  │  1. Connect          │                    │
  │ ──────────────────→  │                    │
  │                      │  2. Relay          │
  │                      │ ─────────────────→ │
  │                      │                    │
  │                      │  3. Response       │
  │                      │ ←───────────────── │
  │  4. Relay            │                    │
  │ ←────────────────────│                    │
  │                      │                    │
  │  Attacker intercepts and potentially      │
  │  modifies all traffic                     │
  │  攻击者拦截并可能修改所有流量             │

Defense: Certificate validation, mutual authentication
防御: 证书验证、双向认证
```

**2. Replay Attack | 重放攻击**
```
Scenario: Online banking
场景: 网上银行

1. Victim sends: "Transfer $100 to Account X"
   受害者发送: "转账$100到账户X"
   
2. Attacker captures the valid message
   攻击者捕获有效消息
   
3. Attacker replays message multiple times
   攻击者多次重放消息
   
   Result: Multiple transfers!
   结果: 多次转账!

Defense: Timestamps, nonces, sequence numbers
防御: 时间戳、随机数、序列号
```

**3. Denial of Service (DoS) | 拒绝服务**
```
Types:
1. Flood Attacks (洪水攻击)
   - SYN flood: Exhaust server connections
   - UDP flood: Overwhelm bandwidth
   - HTTP flood: Application layer flood

2. Amplification Attacks (放大攻击)
   - DNS amplification
   - NTP amplification
   - Small request → Large response

3. Distributed DoS (DDoS) (分布式拒绝服务)
   - Botnet of compromised machines
   - Coordinated attack from multiple sources

Defense: Rate limiting, firewalls, CDN, DDoS protection services
防御: 限流、防火墙、CDN、DDoS防护服务
```

**4. Session Hijacking | 会话劫持**
```
1. Attacker steals session token (cookie, JWT)
   攻击者窃取会话令牌
   
2. Attacker impersonates victim
   攻击者冒充受害者
   
3. Unauthorized access to victim's account
   未授权访问受害者账户

Methods:
- Packet sniffing
- Cross-Site Scripting (XSS)
- Session fixation

Defense: Secure cookies (HttpOnly, Secure), session expiration
防御: 安全Cookie、会话过期
```

**Common Attack Vectors | 常见攻击向量**:

| Attack<br/>攻击               | Type<br/>类型                   | Target<br/>目标                       | Defense<br/>防御                                               |
| ----------------------------- | ------------------------------- | ------------------------------------- | -------------------------------------------------------------- |
| **Phishing<br/>钓鱼**         | Social Engineering<br/>社会工程 | Users<br/>用户                        | Security awareness training<br/>安全意识培训                   |
| **SQL Injection<br/>SQL注入** | Active<br/>主动                 | Web apps<br/>Web应用                  | Input validation, prepared statements<br/>输入验证、预编译语句 |
| **XSS<br/>跨站脚本**          | Active<br/>主动                 | Web apps<br/>Web应用                  | Output encoding, CSP<br/>输出编码、CSP                         |
| **Brute Force<br/>暴力破解**  | Active<br/>主动                 | Authentication<br/>认证               | Account lockout, rate limiting<br/>账户锁定、限流              |
| **Zero-Day<br/>零日攻击**     | Active<br/>主动                 | Software vulnerabilities<br/>软件漏洞 | Patching, IDS/IPS<br/>补丁、入侵检测/防御                      |

**中文:**

**攻击类型**:
- **被动攻击**: 窃听、流量分析（难检测、违反机密性）
- **主动攻击**: 中间人、重放、拒绝服务、会话劫持（易检测、违反完整性和可用性）

**[Exam Focus | 考试重点]**: 
- Differentiate passive vs. active attacks
- Identify attack types and appropriate defenses
- Understand MitM attack mechanism and prevention
- Recognize DoS/DDoS attack types and mitigation

---

## Cryptography Fundamentals | 密码学基础

### 2.1 Symmetric Encryption | 对称加密

**English:**

**Symmetric Encryption** uses the same key for both encryption and decryption. Also known as **secret-key cryptography** or **private-key cryptography**.

**Core Principle | 核心原理**:
```
Sender                                    Receiver
  │                                         │
  │  Shared Secret Key (K)                  │
  │  共享密钥                                │
  │                                         │
  │  Plaintext ──[Encrypt with K]→ Ciphertext
  │  明文                           密文    │
  │                                         │
  │  ─────────── Ciphertext ──────────────→ │
  │                                         │
  │            Ciphertext ──[Decrypt with K]→ Plaintext
  │                                         明文
```

**Symmetric Algorithms | 对称算法**:

#### 1. DES (Data Encryption Standard) | 数据加密标准

**Specifications | 规格**:
- **Key Size**: 56 bits (64 bits with parity)
- **Block Size**: 64 bits
- **Structure**: Feistel network (16 rounds)
- **Status**: **Deprecated** (insecure due to small key size)

**Security | 安全性**:
```
Brute Force Attack:
- 2^56 = 72 quadrillion possible keys
- Modern hardware: <24 hours to break

Result: DES is no longer secure
结果: DES不再安全
```

#### 2. 3DES (Triple DES) | 三重DES

**Principle | 原理**: Apply DES encryption three times with different keys
```
Ciphertext = DES_encrypt(K3, DES_decrypt(K2, DES_encrypt(K1, Plaintext)))

Key Options:
- 3-key 3DES: K1, K2, K3 all different (168 bits effective)
- 2-key 3DES: K1 = K3 (112 bits effective)
```

**Status | 状态**: Being phased out, replaced by AES

#### 3. AES (Advanced Encryption Standard) | 高级加密标准

**Specifications | 规格**:
- **Key Sizes**: 128, 192, 256 bits
- **Block Size**: 128 bits
- **Structure**: Substitution-Permutation Network (SPN)
- **Rounds**: 10 (AES-128), 12 (AES-192), 14 (AES-256)

**AES Encryption Round | AES加密轮次**:
```
Each Round (except last):
1. SubBytes (字节替换): S-box substitution
2. ShiftRows (行移位): Circular shift
3. MixColumns (列混淆): Matrix multiplication
4. AddRoundKey (轮密钥加): XOR with round key

Last Round: Omits MixColumns
最后一轮: 省略列混淆
```

**AES Advantages | AES优势**:
```
✓ Strong security (no practical attacks)
✓ Fast in software and hardware
✓ Widely supported
✓ NIST standard

✓ 强大的安全性（无实际攻击）
✓ 软件和硬件速度快
✓ 广泛支持
✓ NIST标准
```

**Block Cipher Modes of Operation | 分组密码工作模式**:

**1. ECB (Electronic Codebook) | 电子密码本**
```
Plaintext Blocks: P1, P2, P3, P4
                   │   │   │   │
              ┌────▼───▼───▼───▼────┐
              │   Encrypt with K    │
              │   使用K加密         │
              └────┬───┬───┬───┬────┘
                   │   │   │   │
Ciphertext Blocks: C1, C2, C3, C4

Problems:
✗ Identical plaintext blocks → identical ciphertext
✗ Patterns visible in ciphertext
✗ NOT recommended for use

问题:
✗ 相同明文块→相同密文
✗ 密文中可见模式
✗ 不推荐使用
```

**2. CBC (Cipher Block Chaining) | 密码块链接**
```
IV (Initialization Vector)
 │
 │  P1      P2      P3      P4
 │  │       │       │       │
 └→⊕       ⊕       ⊕       ⊕
    │       │       │       │
 ┌──▼───┐ ┌▼───┐ ┌▼───┐ ┌▼───┐
 │Encrypt│ │Enc │ │Enc │ │Enc │
 │  K    │ │ K  │ │ K  │ │ K  │
 └──┬───┘ └┬───┘ └┬───┘ └┬───┘
    │      │      │      │
    C1─────┘      │      │
           C2─────┘      │
                  C3─────┘
                         C4

Advantages:
✓ Same plaintext → different ciphertext (due to IV)
✓ Most common mode
✓ Error propagation (1 bit error affects 2 blocks)

优势:
✓ 相同明文→不同密文（由于IV）
✓ 最常用模式
✓ 错误传播（1位错误影响2个块）
```

**3. CTR (Counter) | 计数器**
```
Nonce + Counter:  N+0    N+1    N+2    N+3
                   │      │      │      │
                ┌──▼───┐ ┌▼───┐ ┌▼───┐ ┌▼───┐
                │Encrypt│ │Enc │ │Enc │ │Enc │
                │  K    │ │ K  │ │ K  │ │ K  │
                └──┬───┘ └┬───┘ └┬───┘ └┬───┘
                   │      │      │      │
Plaintext:         P1     P2     P3     P4
                   │      │      │      │
                   ⊕      ⊕      ⊕      ⊕
                   │      │      │      │
Ciphertext:        C1     C2     C3     C4

Advantages:
✓ Parallelizable (fast)
✓ No error propagation
✓ Random access to blocks
✓ Used in modern protocols (TLS 1.3)

优势:
✓ 可并行化（快速）
✓ 无错误传播
✓ 块的随机访问
✓ 现代协议中使用（TLS 1.3）
```

**4. GCM (Galois/Counter Mode) | Galois/计数器模式**
```
GCM = CTR mode + Authentication (GMAC)

Provides:
✓ Encryption (confidentiality)
✓ Authentication (integrity)
✓ AEAD (Authenticated Encryption with Associated Data)

提供:
✓ 加密（机密性）
✓ 认证（完整性）
✓ AEAD（带关联数据的认证加密）

Used in: TLS 1.2+, IPSec, SSH
用于: TLS 1.2+、IPSec、SSH
```

**Symmetric Key Distribution Problem | 对称密钥分发问题**:

```
Problem: How to securely share the secret key?
问题: 如何安全共享密钥?

Challenges:
1. Key must be transmitted securely (catch-22)
   密钥必须安全传输（悖论）
   
2. Each pair of users needs unique key
   每对用户需要唯一密钥
   
   n users → n(n-1)/2 keys
   
   Example: 100 users → 4,950 keys!
   示例: 100用户 → 4,950个密钥!

Solutions:
- Diffie-Hellman key exchange (密钥交换)
- Key Distribution Center (KDC) (密钥分发中心)
- Public-key cryptography for key transport (公钥密码用于密钥传输)
```

**Symmetric Encryption Comparison | 对称加密对比**:

| Algorithm<br/>算法 | Key Size<br/>密钥大小 | Block Size<br/>块大小 | Security<br/>安全性  | Speed<br/>速度     | Status<br/>状态        |
| ------------------ | --------------------- | --------------------- | -------------------- | ------------------ | ---------------------- |
| **DES**            | 56 bits               | 64 bits               | Weak<br/>弱          | Fast<br/>快        | Deprecated<br/>已弃用  |
| **3DES**           | 112/168 bits          | 64 bits               | Adequate<br/>足够    | Slow<br/>慢        | Phasing out<br/>淘汰中 |
| **AES-128**        | 128 bits              | 128 bits              | Strong<br/>强        | Very Fast<br/>很快 | Recommended<br/>推荐   |
| **AES-256**        | 256 bits              | 128 bits              | Very Strong<br/>很强 | Fast<br/>快        | Recommended<br/>推荐   |

**中文:**

**对称加密**使用相同密钥进行加密和解密。

**主流算法**: DES（已弃用）、3DES（淘汰中）、AES（推荐）

**工作模式**: ECB（不推荐）、CBC（常用）、CTR（可并行）、GCM（带认证）

**密钥分发问题**: n用户需要n(n-1)/2个密钥

**[Exam Focus | 考试重点]**: 
- Compare DES, 3DES, AES (key size, security, speed)
- Understand block cipher modes (ECB, CBC, CTR, GCM)
- Recognize symmetric key distribution problem
- Calculate number of keys for n users: n(n-1)/2

### 2.2 Asymmetric Encryption | 非对称加密

**English:**

**Asymmetric Encryption** (Public-Key Cryptography) uses a pair of keys: **public key** for encryption, **private key** for decryption.

**Core Principle | 核心原理**:
```
Sender                                    Receiver
  │                                         │
  │  Receiver's Public Key (Pub_R)          │  Private Key (Priv_R)
  │  接收者公钥                              │  私钥
  │                                         │
  │  Plaintext ──[Encrypt with Pub_R]→ Ciphertext
  │  明文                              密文  │
  │                                         │
  │  ─────────── Ciphertext ──────────────→ │
  │                                         │
  │            Ciphertext ──[Decrypt with Priv_R]→ Plaintext
  │                                         明文

Key Properties:
1. Public key can be freely distributed
   公钥可自由分发
   
2. Computationally infeasible to derive private key from public key
   从公钥推导私钥在计算上不可行
   
3. What one key encrypts, only the other can decrypt
   一个密钥加密的内容只有另一个密钥能解密
```

**Asymmetric Algorithms | 非对称算法**:

#### 1. RSA (Rivest-Shamir-Adleman) | RSA算法

**Mathematical Foundation | 数学基础**:
```
Based on difficulty of factoring large prime numbers
基于大素数分解的困难性

Key Generation:
1. Select two large primes: p, q
   选择两个大素数: p, q
   
2. Compute n = p × q (modulus)
   计算 n = p × q（模数）
   
3. Compute φ(n) = (p-1) × (q-1) (Euler's totient)
   计算 φ(n) = (p-1) × (q-1)（欧拉函数）
   
4. Choose e (public exponent): 1 < e < φ(n), gcd(e, φ(n)) = 1
   选择 e（公开指数）: 1 < e < φ(n), gcd(e, φ(n)) = 1
   
   Common choice: e = 65537 (0x10001)
   常用选择: e = 65537
   
5. Compute d (private exponent): d × e ≡ 1 (mod φ(n))
   计算 d（私有指数）: d × e ≡ 1 (mod φ(n))

Public Key: (n, e)
Private Key: (n, d)
```

**RSA Encryption/Decryption | RSA加密/解密**:
```
Encryption:
C = M^e mod n

Decryption:
M = C^d mod n

Example:
p = 61, q = 53
n = p × q = 3233
φ(n) = (61-1) × (53-1) = 3120
e = 17 (choose)
d = 2753 (calculate: 17 × 2753 ≡ 1 mod 3120)

Encrypt M = 123:
C = 123^17 mod 3233 = 855

Decrypt C = 855:
M = 855^2753 mod 3233 = 123 ✓
```

**RSA Key Sizes | RSA密钥大小**:
```
Key Size:      Security Level:          Status:
1024 bits      Weak                     Deprecated (deprecated)
2048 bits      Adequate                 Minimum recommended (最低推荐)
3072 bits      Strong                   Good (好)
4096 bits      Very Strong              Future-proof (面向未来)

Note: Larger keys = slower performance
注意: 更大密钥 = 更慢性能
```

#### 2. ECC (Elliptic Curve Cryptography) | 椭圆曲线密码

**Advantages over RSA | 相比RSA的优势**:
```
✓ Smaller key sizes for equivalent security
✓ Faster operations
✓ Lower power consumption (good for mobile/IoT)

Key Size Comparison:
更小的密钥大小实现等效安全性

RSA 2048 bits  ≈  ECC 224 bits
RSA 3072 bits  ≈  ECC 256 bits
RSA 7680 bits  ≈  ECC 384 bits
RSA 15360 bits ≈  ECC 521 bits
```

**Popular ECC Curves | 流行的ECC曲线**:
```
- NIST P-256 (secp256r1): Most widely used (最广泛使用)
- NIST P-384 (secp384r1): Higher security
- Curve25519: Modern, efficient (Ed25519 for signatures)
- secp256k1: Used in Bitcoin
```

#### 3. Diffie-Hellman Key Exchange | Diffie-Hellman密钥交换

**Purpose | 目的**: Securely establish shared secret over insecure channel

**Protocol | 协议**:
```
Public Parameters (known to all):
- Prime number p
- Generator g

Alice                                    Bob
  │                                       │
  │  1. Choose private key a              │  2. Choose private key b
  │     (random)                          │     (random)
  │                                       │
  │  3. Compute public key:               │  4. Compute public key:
  │     A = g^a mod p                     │     B = g^b mod p
  │                                       │
  │  5. Send A ─────────────────────────→ │
  │                                       │
  │  ←───────────────────────── Send B    │  6. Send B
  │                                       │
  │  7. Compute shared secret:            │  8. Compute shared secret:
  │     s = B^a mod p                     │     s = A^b mod p
  │                                       │
  │  Both have same shared secret:        │
  │  s = (g^b)^a mod p = (g^a)^b mod p = g^(ab) mod p

Example:
p = 23, g = 5
Alice: a = 6 → A = 5^6 mod 23 = 8
Bob:   b = 15 → B = 5^15 mod 23 = 19

Alice: s = 19^6 mod 23 = 2
Bob:   s = 8^15 mod 23 = 2

Shared secret = 2 ✓
```

**Security | 安全性**:
```
Eavesdropper knows: p, g, A, B
Eavesdropper does NOT know: a, b

To break: Must solve Discrete Logarithm Problem (DLP)
破解: 必须解决离散对数问题（DLP）

Computationally infeasible for large p
对于大的p在计算上不可行
```

**Vulnerability: Man-in-the-Middle | 漏洞: 中间人攻击**:
```
Without authentication, attacker can intercept:

Alice ←→ Attacker ←→ Bob

Alice thinks she's talking to Bob
Bob thinks he's talking to Alice
But attacker controls both connections!

Solution: Authenticated Diffie-Hellman (using certificates)
解决方案: 认证的Diffie-Hellman（使用证书）
```

**Symmetric vs. Asymmetric Comparison | 对称vs非对称对比**:

| Aspect<br/>方面                   | Symmetric<br/>对称                    | Asymmetric<br/>非对称                                   |
| --------------------------------- | ------------------------------------- | ------------------------------------------------------- |
| **Keys<br/>密钥**                 | One shared key<br/>一个共享密钥       | Public/private key pair<br/>公钥/私钥对                 |
| **Key Distribution<br/>密钥分发** | Difficult (n(n-1)/2 keys)<br/>困难    | Easy (public key distributed)<br/>容易                  |
| **Speed<br/>速度**                | Very fast<br/>很快                    | Slow (100-1000x slower)<br/>慢                          |
| **Key Size<br/>密钥大小**         | Smaller (128-256 bits)<br/>较小       | Larger (2048-4096 bits)<br/>较大                        |
| **Use Case<br/>使用场景**         | Bulk data encryption<br/>批量数据加密 | Key exchange, digital signatures<br/>密钥交换、数字签名 |
| **Examples<br/>示例**             | AES, DES, 3DES                        | RSA, ECC, Diffie-Hellman                                |

**Hybrid Encryption | 混合加密**:

```
Best of Both Worlds (used in SSL/TLS, PGP):
结合两者优势（SSL/TLS、PGP中使用）:

1. Use asymmetric encryption for key exchange
   使用非对称加密进行密钥交换
   - Generate random symmetric session key
   - Encrypt session key with recipient's public key

2. Use symmetric encryption for data
   使用对称加密加密数据
   - Encrypt bulk data with session key (fast)
   
3. Send both encrypted session key and encrypted data
   发送加密的会话密钥和加密的数据

Example:
Alice → Bob:
1. Generate AES-256 session key (K_session)
2. Encrypt K_session with Bob's RSA public key
3. Encrypt message with K_session (AES)
4. Send: RSA(K_session) + AES(message)

Bob receives:
1. Decrypt K_session with his RSA private key
2. Decrypt message with K_session

Performance: Fast encryption + secure key exchange!
性能: 快速加密 + 安全密钥交换!
```

**中文:**

**非对称加密**（公钥密码）使用一对密钥：公钥用于加密，私钥用于解密。

**主流算法**: RSA、ECC、Diffie-Hellman

**优势**: 简化密钥分发、支持数字签名

**缺点**: 速度慢（比对称加密慢100-1000倍）

**混合加密**: 结合对称和非对称加密优势（用于SSL/TLS、PGP）

**[Exam Focus | 考试重点]**: 
- Understand RSA key generation and encryption/decryption
- Compare RSA vs. ECC key sizes
- Explain Diffie-Hellman key exchange protocol
- Recognize MitM vulnerability in DH (need authentication)
- Understand hybrid encryption (asymmetric for key, symmetric for data)
- Compare symmetric vs. asymmetric (speed, key distribution, use cases)

### 2.3 Hash Functions and Digital Signatures | 哈希函数与数字签名

**English:**

**Hash Functions | 哈希函数**

**Definition | 定义**: A hash function takes an input of arbitrary length and produces a fixed-length output (hash value or message digest).

**Properties | 属性**:
```
1. Deterministic (确定性)
   - Same input always produces same hash
   - 相同输入始终产生相同哈希

2. Fast Computation (快速计算)
   - Efficient to compute hash
   - 高效计算哈希

3. Pre-image Resistance (原像抗性)
   - Given hash h, hard to find message m such that hash(m) = h
   - 给定哈希h，难以找到消息m使得hash(m) = h
   - One-way function (单向函数)

4. Second Pre-image Resistance (第二原像抗性)
   - Given m1, hard to find m2 (m2 ≠ m1) such that hash(m1) = hash(m2)
   - 给定m1，难以找到m2使得hash(m1) = hash(m2)

5. Collision Resistance (抗碰撞性)
   - Hard to find any two messages m1, m2 where hash(m1) = hash(m2)
   - 难以找到任意两个消息m1、m2使得hash(m1) = hash(m2)
   - Strongest property (最强属性)
```

**Hash Algorithms | 哈希算法**:

#### 1. MD5 (Message Digest 5) | 消息摘要5

**Specifications | 规格**:
- **Output Size**: 128 bits (16 bytes)
- **Status**: **Broken** (collision attacks practical)

**Example | 示例**:
```
Input:  "Hello, World!"
MD5:    65a8e27d8879283831b664bd8b7f0ad4

Input:  "Hello, World"  (one character difference)
MD5:    bea8252ff4e80f41719ea13cdf007273
                       ↑ Completely different hash
```

**Security Issues | 安全问题**:
```
✗ Collision attacks found (2004)
✗ Can generate two different files with same MD5
✗ Not suitable for security applications

✗ 发现碰撞攻击（2004年）
✗ 可以生成两个不同文件具有相同MD5
✗ 不适合安全应用
```

#### 2. SHA-1 (Secure Hash Algorithm 1) | 安全哈希算法1

**Specifications | 规格**:
- **Output Size**: 160 bits (20 bytes)
- **Status**: **Deprecated** (collision attack demonstrated in 2017)

**Example | 示例**:
```
Input:  "Hello, World!"
SHA-1:  0a0a9f2a6772942557ab5355d76af442f8f65e01
```

**Security Issues | 安全问题**:
```
✗ Google demonstrated collision attack (SHAttered, 2017)
✗ No longer accepted by browsers for certificates
✗ Use SHA-256 or higher instead

✗ Google演示了碰撞攻击（SHAttered，2017）
✗ 浏览器不再接受用于证书
✗ 改用SHA-256或更高
```

#### 3. SHA-2 Family (SHA-256, SHA-384, SHA-512) | SHA-2家族

**Specifications | 规格**:
```
Algorithm     Output Size    Block Size    Rounds
SHA-224       224 bits       512 bits      64
SHA-256       256 bits       512 bits      64    ← Most common
SHA-384       384 bits       1024 bits     80
SHA-512       512 bits       1024 bits     80
```

**SHA-256 Example | SHA-256示例**:
```
Input:  "Hello, World!"
SHA-256: dffd6021bb2bd5b0af676290809ec3a53191dd81c7f70a4b28688a362182986f
```

**Status | 状态**: Currently secure, widely used (TLS, Bitcoin, etc.)

#### 4. SHA-3 | SHA-3

**Specifications | 规格**:
- **Output Sizes**: 224, 256, 384, 512 bits
- **Structure**: Keccak sponge construction (different from SHA-2)
- **Status**: NIST standard (2015), gaining adoption

**Hash Function Comparison | 哈希函数对比**:

| Algorithm<br/>算法 | Output Size<br/>输出大小 | Security<br/>安全性  | Speed<br/>速度     | Status<br/>状态         |
| ------------------ | ------------------------ | -------------------- | ------------------ | ----------------------- |
| **MD5**            | 128 bits                 | Broken<br/>已破解    | Very Fast<br/>很快 | Do NOT use<br/>不要使用 |
| **SHA-1**          | 160 bits                 | Weak<br/>弱          | Fast<br/>快        | Deprecated<br/>已弃用   |
| **SHA-256**        | 256 bits                 | Strong<br/>强        | Fast<br/>快        | Recommended<br/>推荐    |
| **SHA-512**        | 512 bits                 | Very Strong<br/>很强 | Moderate<br/>中等  | Recommended<br/>推荐    |
| **SHA-3**          | 224-512 bits             | Strong<br/>强        | Fast<br/>快        | Emerging<br/>新兴       |

**Digital Signatures | 数字签名**

**Purpose | 目的**: Provide authentication, integrity, and non-repudiation.

**How Digital Signatures Work | 数字签名工作原理**:

**Signing Process | 签名过程**:
```
Signer (Alice)
  │
  │  1. Hash the message
  │     Message ──[SHA-256]→ Hash (32 bytes)
  │     消息                   哈希
  │
  │  2. Encrypt hash with private key
  │     Hash ──[RSA Private Key]→ Digital Signature
  │     哈希                       数字签名
  │
  │  3. Send message + signature
  │     ────────────────────────────────→
```

**Verification Process | 验证过程**:
```
Verifier (Bob)
  │
  │  1. Receive message + signature
  │     ←────────────────────────────────
  │
  │  2. Hash the received message
  │     Message ──[SHA-256]→ Hash A
  │     消息                   哈希A
  │
  │  3. Decrypt signature with public key
  │     Signature ──[RSA Public Key]→ Hash B
  │     签名                           哈希B
  │
  │  4. Compare Hash A == Hash B?
  │     If yes: Signature valid, message authentic
  │     如果是: 签名有效、消息真实
  │     If no:  Signature invalid, message tampered
  │     如果否: 签名无效、消息被篡改
```

**Complete Example | 完整示例**:
```
Alice wants to sign message "Transfer $100 to Bob"

1. Hash message:
   SHA-256("Transfer $100 to Bob") = abc123def...

2. Sign hash:
   Signature = RSA_sign(abc123def..., Alice_Private_Key)
   
3. Send to Bob:
   Message: "Transfer $100 to Bob"
   Signature: xyz789...
   
Bob verifies:
1. Hash received message:
   SHA-256("Transfer $100 to Bob") = abc123def...
   
2. Decrypt signature:
   Hash_from_sig = RSA_verify(xyz789..., Alice_Public_Key)
   Hash_from_sig = abc123def...
   
3. Compare:
   abc123def... == abc123def... ✓
   
   Signature valid! Message is from Alice and unaltered.
   签名有效！消息来自Alice且未被篡改。
```

**Digital Signature vs. Encryption | 数字签名vs加密**:

| Aspect<br/>方面                  | Encryption<br/>加密                   | Digital Signature<br/>数字签名                                          |
| -------------------------------- | ------------------------------------- | ----------------------------------------------------------------------- |
| **Purpose<br/>目的**             | Confidentiality<br/>机密性            | Authentication, Integrity, Non-repudiation<br/>认证、完整性、不可否认性 |
| **Sender uses<br/>发送者使用**   | Receiver's public key<br/>接收者公钥  | Sender's private key<br/>发送者私钥                                     |
| **Receiver uses<br/>接收者使用** | Receiver's private key<br/>接收者私钥 | Sender's public key<br/>发送者公钥                                      |
| **Output<br/>输出**              | Ciphertext<br/>密文                   | Signature<br/>签名                                                      |

**Signature Algorithms | 签名算法**:

**1. RSA Signature | RSA签名**:
```
Sign:   S = Hash(M)^d mod n  (use private key)
Verify: Hash(M) == S^e mod n  (use public key)
```

**2. DSA (Digital Signature Algorithm) | 数字签名算法**:
- Based on discrete logarithm problem
- Separate algorithm specifically for signatures (not encryption)
- 基于离散对数问题
- 专门用于签名的独立算法（不用于加密）

**3. ECDSA (Elliptic Curve DSA) | 椭圆曲线DSA**:
- DSA using elliptic curves
- Smaller signatures, faster than RSA
- Used in Bitcoin, TLS, SSH
- 使用椭圆曲线的DSA
- 更小的签名、比RSA更快
- 用于Bitcoin、TLS、SSH

**Message Authentication Code (MAC) | 消息认证码**:

**HMAC (Hash-based MAC) | 基于哈希的MAC**:

**Purpose | 目的**: Verify integrity and authenticity using shared secret key (symmetric).

**Formula | 公式**:
```
HMAC(K, M) = Hash((K ⊕ opad) || Hash((K ⊕ ipad) || M))

Where:
K = secret key (密钥)
M = message (消息)
opad = outer padding (外部填充)
ipad = inner padding (内部填充)
|| = concatenation (连接)
⊕ = XOR

Example:
HMAC-SHA256(K="secret", M="data") = 5d41...
```

**HMAC vs. Digital Signature | HMAC vs 数字签名**:

| Aspect<br/>方面                    | HMAC<br/>HMAC                                                    | Digital Signature<br/>数字签名                        |
| ---------------------------------- | ---------------------------------------------------------------- | ----------------------------------------------------- |
| **Cryptography<br/>密码学**        | Symmetric<br/>对称                                               | Asymmetric<br/>非对称                                 |
| **Key<br/>密钥**                   | Shared secret<br/>共享密钥                                       | Public/private pair<br/>公钥/私钥对                   |
| **Non-repudiation<br/>不可否认性** | No (both parties have key)<br/>否（双方都有密钥）                | Yes<br/>是                                            |
| **Speed<br/>速度**                 | Fast<br/>快                                                      | Slow<br/>慢                                           |
| **Use Case<br/>使用场景**          | TLS record protocol, API authentication<br/>TLS记录协议、API认证 | Email signatures, code signing<br/>邮件签名、代码签名 |

**中文:**

**哈希函数**: 将任意长度输入转换为固定长度输出（消息摘要）

**主流哈希算法**: MD5（已破解）、SHA-1（已弃用）、SHA-256（推荐）、SHA-512、SHA-3

**数字签名**: 提供认证、完整性、不可否认性

**签名过程**: 哈希消息 → 用私钥加密哈希 → 得到签名

**验证过程**: 哈希消息 → 用公钥解密签名 → 对比哈希

**签名算法**: RSA签名、DSA、ECDSA

**HMAC**: 基于哈希的消息认证码（对称密钥）

**[Exam Focus | 考试重点]**: 
- Compare hash algorithms (MD5, SHA-1, SHA-256)
- Understand hash properties (pre-image resistance, collision resistance)
- Explain digital signature process (signing and verification)
- Differentiate digital signature vs. encryption (purpose, key usage)
- Compare HMAC vs. digital signature (symmetric vs. asymmetric)
- Recognize use cases for each

---

## SSL/TLS Protocol | SSL/TLS协议

### 3.1 SSL/TLS Overview | SSL/TLS概述

**English:**

**SSL (Secure Sockets Layer)** and **TLS (Transport Layer Security)** are cryptographic protocols designed to provide secure communication over a computer network.

**History and Evolution | 历史与演进**:

```
1994: SSL 1.0 (never released, internal only)
      SSL 1.0（从未发布、仅内部）

1995: SSL 2.0 (released by Netscape)
      SSL 2.0（Netscape发布）
      - Serious security flaws
      - 严重安全缺陷

1996: SSL 3.0 (major redesign)
      SSL 3.0（重大重新设计）
      - Foundation for TLS
      - TLS的基础

1999: TLS 1.0 (IETF standard, RFC 2246)
      TLS 1.0（IETF标准）
      - Based on SSL 3.0
      - Minor improvements

2006: TLS 1.1 (RFC 4346)
      - Protection against CBC attacks
      - 防护CBC攻击

2008: TLS 1.2 (RFC 5246)
      - Support for AE AD ciphers (GCM)
      - SHA-256 instead of MD5/SHA-1
      - 支持AEAD密码
      - SHA-256替代MD5/SHA-1

2018: TLS 1.3 (RFC 8446)
      - Simplified handshake (1-RTT)
      - Removed legacy ciphers
      - Mandatory Perfect Forward Secrecy
      - 简化握手（1-RTT）
      - 移除遗留密码
      - 强制完美前向保密

Current Recommendations (2024):
- TLS 1.2: Minimum acceptable
- TLS 1.3: Preferred
- SSL 2.0/3.0, TLS 1.0/1.1: Deprecated/disabled

当前建议（2024）:
- TLS 1.2: 最低可接受
- TLS 1.3: 首选
- SSL 2.0/3.0、TLS 1.0/1.1: 已弃用/禁用
```

**Protocol Position in OSI Model | 协议在OSI模型中的位置**:

```
┌────────────────────────────────────┐
│   Application Layer (HTTP, FTP)   │
│   应用层                           │
├────────────────────────────────────┤
│   SSL/TLS (Presentation Layer)    │
│   SSL/TLS（表示层）                │
│   - Encryption                     │
│   - Authentication                 │
│   - 加密                           │
│   - 认证                           │
├────────────────────────────────────┤
│   Transport Layer (TCP)            │
│   传输层                           │
└────────────────────────────────────┘

Typical Use:
HTTP + TLS = HTTPS (port 443)
SMTP + TLS = SMTPS (port 465/587)
FTP + TLS = FTPS (port 990)

典型使用:
HTTP + TLS = HTTPS（端口443）
SMTP + TLS = SMTPS（端口465/587）
FTP + TLS = FTPS（端口990）
```

**SSL/TLS Goals | SSL/TLS目标**:

**1. Confidentiality | 机密性**
```
- Encrypt data to prevent eavesdropping
- Use symmetric encryption (AES)
- 加密数据以防止窃听
- 使用对称加密（AES）
```

**2. Integrity | 完整性**
```
- Detect tampering with MAC
- Use HMAC or AEAD
- 使用MAC检测篡改
- 使用HMAC或AEAD
```

**3. Authentication | 认证**
```
- Verify server identity (always)
- Verify client identity (optional, mutual TLS)
- Use digital certificates (X.509)
- 验证服务器身份（始终）
- 验证客户端身份（可选、双向TLS）
- 使用数字证书（X.509）
```

**SSL/TLS Protocol Architecture | SSL/TLS协议架构**:

```
┌─────────────────────────────────────────────────────────┐
│            SSL/TLS Protocol Suite                       │
│            SSL/TLS协议套件                              │
├───────────────┬─────────────────────┬───────────────────┤
│  Handshake    │  Change Cipher Spec │   Alert Protocol  │
│  Protocol     │  Protocol           │   警报协议        │
│  握手协议     │  密码规格变更协议   │                   │
│               │                     │                   │
│  - Negotiate  │  - Signal cipher    │  - Error handling │
│    parameters │    switch           │  - Warnings       │
│  - Authenticate│  - 信号密码切换     │  - 错误处理       │
│  - Exchange   │                     │  - 警告           │
│    keys       │                     │                   │
│  - 协商参数   │                     │                   │
│  - 认证       │                     │                   │
│  - 交换密钥   │                     │                   │
├───────────────┴─────────────────────┴───────────────────┤
│               Record Protocol                           │
│               记录协议                                  │
│                                                         │
│  - Fragment data into records                          │
│  - Compress (optional, removed in TLS 1.3)             │
│  - Add MAC                                              │
│  - Encrypt                                              │
│  - 将数据分段为记录                                    │
│  - 压缩（可选、TLS 1.3中移除）                         │
│  - 添加MAC                                              │
│  - 加密                                                 │
└─────────────────────────────────────────────────────────┘
          ↓
┌─────────────────────────────────────────────────────────┐
│               TCP (Reliable Transport)                  │
│               TCP（可靠传输）                           │
└─────────────────────────────────────────────────────────┘
```

**中文:**

**SSL/TLS**是设计用于在计算机网络上提供安全通信的密码协议。

**演进**: SSL 2.0 → SSL 3.0 → TLS 1.0 → TLS 1.2 → TLS 1.3

**协议位置**: 应用层和传输层之间（表示层）

**目标**: 机密性、完整性、认证

**协议组成**: 握手协议、记录协议、密码规格变更协议、警报协议

**[Exam Focus | 考试重点]**: 
- Understand SSL/TLS evolution (SSL 3.0 → TLS 1.0 → TLS 1.2 → TLS 1.3)
- Recognize protocol position (between application and transport)
- Identify three main goals (confidentiality, integrity, authentication)
- Understand protocol architecture (handshake, record, alert)

### 3.2 TLS Handshake Process | TLS握手过程

**English:**

The **TLS Handshake** establishes secure communication parameters between client and server.

**TLS 1.2 Full Handshake | TLS 1.2完整握手**:

```
Client                                                Server
  │                                                     │
  │  1. ClientHello                                     │
  │  ──────────────────────────────────────────────────→│
  │  - Protocol version: TLS 1.2                        │
  │  - Random (32 bytes): Client Random                 │
  │  - Session ID (for resumption)                      │
  │  - Cipher suites supported:                         │
  │    [TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256,          │
  │     TLS_RSA_WITH_AES_256_CBC_SHA, ...]              │
  │  - Compression methods (null)                       │
  │  - Extensions:                                      │
  │    - server_name (SNI): www.example.com             │
  │    - supported_groups (elliptic curves)             │
  │    - signature_algorithms                           │
  │                                                     │
  │                                  2. ServerHello     │
  │  ←──────────────────────────────────────────────────│
  │                        - Protocol version: TLS 1.2  │
  │                        - Random (32 bytes): Server  │
  │                        - Session ID (new or resumed)│
  │                        - Cipher suite selected:     │
  │                          TLS_ECDHE_RSA_WITH_AES_128_│
  │                          GCM_SHA256                 │
  │                        - Compression: null          │
  │                        - Extensions                 │
  │                                                     │
  │                                3. Certificate       │
  │  ←──────────────────────────────────────────────────│
  │                        - Server's X.509 certificate │
  │                        - Certificate chain          │
  │                        - 服务器X.509证书            │
  │                        - 证书链                     │
  │                                                     │
  │                            4. ServerKeyExchange     │
  │  ←──────────────────────────────────────────────────│
  │                   (Only for DHE/ECDHE key exchange) │
  │                   - ECDH parameters                 │
  │                   - Signature over parameters       │
  │                   - 仅用于DHE/ECDHE密钥交换         │
  │                   - ECDH参数                        │
  │                   - 参数签名                        │
  │                                                     │
  │                            5. CertificateRequest    │
  │  ←──────────────────────────────────────────────────│
  │                                   (Optional, mTLS)  │
  │                   - Certificate types               │
  │                   - Acceptable CAs                  │
  │                                                     │
  │                            6. ServerHelloDone       │
  │  ←──────────────────────────────────────────────────│
  │                                                     │
  │  7. Certificate (if requested)                      │
  │  ──────────────────────────────────────────────────→│
  │  - Client's certificate                             │
  │                                                     │
  │  8. ClientKeyExchange                               │
  │  ──────────────────────────────────────────────────→│
  │  - ECDH public key                                  │
  │  - Or encrypted pre-master secret (RSA)             │
  │  - ECDH公钥                                         │
  │  - 或加密的预主密钥（RSA）                          │
  │                                                     │
  │  9. CertificateVerify (if client cert sent)          │
  │  ──────────────────────────────────────────────────→│
  │  - Signature over all handshake messages            │
  │  - 所有握手消息的签名                               │
  │                                                     │
  │  Both sides compute Master Secret from:             │
  │  - Pre-Master Secret (from key exchange)            │
  │  - Client Random                                    │
  │  - Server Random                                    │
  │  双方从以下计算主密钥:                              │
  │  - 预主密钥（来自密钥交换）                         │
  │  - 客户端随机数                                     │
  │  - 服务器随机数                                     │
  │                                                     │
  │  10. ChangeCipherSpec                               │
  │  ──────────────────────────────────────────────────→│
  │  (Signal: switching to encrypted communication)     │
  │  （信号: 切换到加密通信）                           │
  │                                                     │
  │  11. Finished (encrypted with session keys)         │
  │  ──────────────────────────────────────────────────→│
  │  - MAC of all handshake messages                    │
  │  - Verify handshake integrity                       │
  │  - 所有握手消息的MAC                                │
  │  - 验证握手完整性                                   │
  │                                                     │
  │                        12. ChangeCipherSpec         │
  │  ←──────────────────────────────────────────────────│
  │                                                     │
  │                        13. Finished (encrypted)     │
  │  ←──────────────────────────────────────────────────│
  │                                                     │
  │  ══════════ Secure Channel Established ══════════   │
  │  ══════════ 安全通道已建立 ══════════               │
  │                                                     │
  │  Application Data (encrypted)                       │
  │  ←─────────────────────────────────────────────────→│
  │  应用数据（加密）                                   │
```

**Key Generation Process | 密钥生成过程**:

```
1. Pre-Master Secret Generation:
   预主密钥生成:

   RSA Key Exchange:
   - Client generates 48-byte random number
   - Encrypts with server's RSA public key
   - 客户端生成48字节随机数
   - 用服务器RSA公钥加密

   ECDHE Key Exchange (Preferred):
   - Both parties perform Diffie-Hellman
   - Compute shared secret
   - 双方执行Diffie-Hellman
   - 计算共享密钥

2. Master Secret Derivation:
   主密钥派生:

   Master Secret = PRF(
       Pre-Master Secret,
       "master secret",
       Client Random + Server Random
   )

   PRF = Pseudo-Random Function (based on HMAC)
   PRF = 伪随机函数（基于HMAC）

3. Session Keys Generation:
   会话密钥生成:

   Key Block = PRF(
       Master Secret,
       "key expansion",
       Server Random + Client Random
   )

   From Key Block, extract:
   从密钥块中提取:
   - Client Write MAC Key (客户端写MAC密钥)
   - Server Write MAC Key (服务器写MAC密钥)
   - Client Write Encryption Key (客户端写加密密钥)
   - Server Write Encryption Key (服务器写加密密钥)
   - Client Write IV (客户端写IV)
   - Server Write IV (服务器写IV)
```

**TLS 1.3 Handshake Improvements | TLS 1.3握手改进**:

```
Client                                    Server
  │                                         │
  │  1. ClientHello                         │
  │  + Key Share (ECDHE public key)         │
  │  + Supported Versions (TLS 1.3)         │
  │  ──────────────────────────────────────→│
  │                                         │
  │                      2. ServerHello     │
  │                      + Key Share        │
  │  ←──────────────────────────────────────│
  │                                         │
  │  ──────── Encrypted Handshake ─────────→│
  │                                         │
  │              3. EncryptedExtensions     │
  │              4. Certificate             │
  │              5. CertificateVerify       │
  │              6. Finished                │
  │  ←──────────────────────────────────────│
  │                                         │
  │  7. Finished                            │
  │  ──────────────────────────────────────→│
  │                                         │
  │  Application Data (encrypted)           │
  │  ←─────────────────────────────────────→│

Key Improvements:
关键改进:

✓ 1-RTT handshake (vs 2-RTT in TLS 1.2)
  1-RTT握手（相比TLS 1.2的2-RTT）
  - Faster connection establishment
  - 更快的连接建立

✓ 0-RTT resumption (for returning clients)
  0-RTT恢复（用于返回的客户端）
  - Send data in first flight
  - 在第一次发送中发送数据

✓ Forward Secrecy mandatory
  强制前向保密
  - ECDHE required, RSA key exchange removed
  - 需要ECDHE，移除RSA密钥交换

✓ Simplified cipher suites
  简化密码套件
  - Only AEAD ciphers (AES-GCM, ChaCha20-Poly1305)
  - 仅AEAD密码

✓ Removed legacy features
  移除遗留功能
  - No SSL 2.0/3.0 compatibility
  - No compression
  - No MD5, SHA-1
```

**Session Resumption | 会话恢复**:

**Session ID Resumption | 会话ID恢复**:
```
First Connection:
Client sends: Session ID = empty
Server responds: Session ID = xyz123
Both cache: Master Secret + Session ID

首次连接:
客户端发送: 会话ID = 空
服务器响应: 会话ID = xyz123
双方缓存: 主密钥 + 会话ID

Resumed Connection:
Client sends: Session ID = xyz123
Server recognizes: Reuse cached Master Secret
Skip: Certificate exchange, key exchange
Direct: ChangeCipherSpec + Finished

恢复的连接:
客户端发送: 会话ID = xyz123
服务器识别: 重用缓存的主密钥
跳过: 证书交换、密钥交换
直接: ChangeCipherSpec + Finished

Benefit: ~75% faster handshake
好处: ~75%更快的握手
```

**Session Tickets (RFC 5077) | 会话票据**:
```
Server encrypts session state:
Ticket = Encrypt(Master Secret, Cipher, ..., Server Key)

Server sends ticket to client
Client stores ticket

Resumption:
Client sends ticket in ClientHello
Server decrypts ticket, recovers session
No server-side storage needed!

服务器加密会话状态:
票据 = 加密(主密钥, 密码, ..., 服务器密钥)

服务器将票据发送给客户端
客户端存储票据

恢复:
客户端在ClientHello中发送票据
服务器解密票据、恢复会话
不需要服务器端存储!
```

**中文:**

**TLS握手过程**:
1. ClientHello（客户端问候）
2. ServerHello（服务器问候）
3. Certificate（证书）
4. ServerKeyExchange（服务器密钥交换，ECDHE）
5. ServerHelloDone（服务器问候完成）
6. ClientKeyExchange（客户端密钥交换）
7. ChangeCipherSpec（密码规格变更）
8. Finished（完成）

**密钥生成**: 预主密钥 → 主密钥 → 会话密钥

**TLS 1.3改进**: 1-RTT握手、强制前向保密、简化密码套件、移除遗留功能

**会话恢复**: 会话ID、会话票据（更快的重新连接）

**[Exam Focus | 考试重点]**: 
- Memorize TLS handshake message sequence
- Understand key exchange (RSA vs ECDHE)
- Explain key generation (pre-master → master → session keys)
- Recognize TLS 1.3 improvements (1-RTT, mandatory PFS)
- Understand session resumption mechanisms

---

由于篇幅限制，文档已包含核心安全协议内容。技术文档涵盖信息安全基础（CIA三元组、攻击类型）、密码学基础（对称/非对称加密、哈希函数、数字签名）、SSL/TLS协议（握手过程、密钥生成、TLS 1.3改进），并提供详细的双语说明、协议交互图、密钥生成算法和考试重点标注。完整文档还应包含PGP协议、IPSec协议、协议对比和安全攻击防护等章节。