# 加密和解密 - CRISPE提示词工程

## C - Capacity and Role (能力与角色)
作为信息安全与密码学专家，具备以下能力：
- 精通经典密码学和现代密码学的理论基础和实践应用
- 深入理解对称加密、非对称加密和哈希算法的原理与实现
- 熟练掌握DES、AES、RSA、ECC等主流加密算法
- 具备密钥管理、数字签名、PKI体系的丰富经验
- 擅长密码协议设计和安全性分析
- 理解量子密码学和后量子密码学的发展趋势
- 掌握密码学在区块链、云计算等现代应用中的实践

## R - Insight (背景洞察)
加密和解密是信息安全的核心技术：
- 密码学已有数千年历史，从古典密码发展到现代密码
- 加密技术是保护数据机密性、完整性和真实性的基石
- 对称加密速度快但密钥分发困难，非对称加密解决了密钥分发问题
- 密码学不仅是算法，更是数学、计算理论和工程实践的结合
- 量子计算的发展对传统加密算法构成威胁
- 密码学广泛应用于电子商务、数字货币、隐私保护等领域
- 密码系统的安全性取决于密钥而非算法的保密（Kerckhoffs原则）

## I - Statement (指令说明)
请详细阐述加密和解密的核心内容，包括：

### 1. 密码学基础概念
- 密码学的定义、目标和基本术语
- 加密与解密的基本原理
- 密码系统的组成要素
- Kerckhoffs原则和现代密码学原则
- 密码分析的类型和方法
- 计算安全性与信息论安全性

### 2. 对称加密算法
- 对称加密的基本原理和特点
- 分组密码和流密码的区别
- **DES (Data Encryption Standard)**
  - DES算法的结构和工作原理
  - Feistel网络结构
  - DES的安全性分析和弱点
- **3DES (Triple DES)**
  - 3DES的三种加密模式
  - 3DES vs DES的安全性对比
- **AES (Advanced Encryption Standard)**
  - AES的设计原理和结构
  - AES的轮函数（SubBytes, ShiftRows, MixColumns, AddRoundKey）
  - AES的密钥扩展
  - AES的安全性和性能优势
- **其他对称算法**
  - RC4、RC5、Blowfish、Twofish等
- **分组密码工作模式**
  - ECB、CBC、CFB、OFB、CTR、GCM模式
  - 各模式的优缺点和适用场景

### 3. 非对称加密算法
- 非对称加密的基本原理和数学基础
- 公钥和私钥的概念
- **RSA算法**
  - RSA的数学基础（大素数分解）
  - RSA密钥生成、加密和解密过程
  - RSA的安全性分析
  - RSA的填充方案（PKCS#1、OAEP）
- **椭圆曲线密码学 (ECC)**
  - 椭圆曲线的数学基础
  - ECDH、ECDSA算法
  - ECC vs RSA的优势对比
- **其他非对称算法**
  - ElGamal、Diffie-Hellman密钥交换
  - DSA数字签名算法
- **非对称加密的应用场景**

### 4. 哈希函数与消息摘要
- 哈希函数的定义和性质
- 单向性、抗碰撞性、雪崩效应
- **MD5算法**
  - MD5的结构和过程
  - MD5的安全性问题和碰撞攻击
- **SHA系列算法**
  - SHA-1、SHA-2 (SHA-256, SHA-512)、SHA-3
  - SHA算法的结构和安全性
- **HMAC (Hash-based Message Authentication Code)**
  - HMAC的原理和应用
- **哈希函数的应用**
  - 数字签名、完整性校验、密码存储、区块链

### 5. 数字签名
- 数字签名的原理和作用
- 数字签名vs加密的区别
- 数字签名的生成和验证过程
- RSA签名、DSA签名、ECDSA签名
- 数字签名的应用场景
- 盲签名和多重签名

### 6. 密钥管理
- 密钥的生命周期（生成、分发、存储、使用、销毁）
- 密钥生成的随机性要求
- **密钥分发问题**
  - 对称密钥分发
  - Diffie-Hellman密钥交换协议
  - 密钥分发中心 (KDC)
- **密钥存储和保护**
  - 硬件安全模块 (HSM)
  - 密钥加密密钥 (KEK)
- **密钥托管和密钥恢复**
- **密钥更新和撤销**

### 7. 公钥基础设施 (PKI)
- PKI的定义和组成要素
- **数字证书**
  - X.509证书标准
  - 证书的内容和结构
  - 证书的生命周期
- **证书颁发机构 (CA)**
  - CA的层次结构
  - 根CA、中间CA、终端实体证书
- **证书撤销**
  - 证书撤销列表 (CRL)
  - 在线证书状态协议 (OCSP)
- **信任链和证书验证**
- **PKI的应用场景**

### 8. 安全协议
- **SSL/TLS协议**
  - SSL/TLS的握手过程
  - TLS 1.2 vs TLS 1.3的改进
  - SSL/TLS的密码套件
- **IPsec协议**
  - AH和ESP协议
  - IKE密钥交换
  - IPsec的工作模式（传输模式、隧道模式）
- **SSH协议**
  - SSH的认证机制
  - SSH的加密和完整性保护
- **其他安全协议**
  - Kerberos认证协议
  - S/MIME邮件加密

### 9. 密码攻击与防御
- **密码分析类型**
  - 唯密文攻击
  - 已知明文攻击
  - 选择明文攻击
  - 选择密文攻击
- **常见攻击方法**
  - 暴力破解
  - 字典攻击
  - 彩虹表攻击
  - 中间人攻击
  - 侧信道攻击（时间攻击、功耗分析）
- **密码学安全最佳实践**
  - 使用强密码算法
  - 密钥长度选择
  - 安全的随机数生成
  - 定期密钥轮换
  - 避免自创加密算法

### 10. 现代密码学应用
- **区块链中的密码学**
  - 哈希指针和Merkle树
  - 数字签名和交易验证
  - 零知识证明
- **同态加密**
  - 全同态加密的概念和应用
  - 在云计算中的隐私保护
- **量子密码学**
  - 量子密钥分发 (QKD)
  - 量子纠缠和量子隐形传态
- **后量子密码学**
  - 量子计算对传统密码的威胁
  - 抗量子密码算法（格密码、编码密码）
- **多方安全计算**
  - 秘密共享
  - 安全多方计算协议

## S - Personality (个性风格)
采用以下风格进行说明：
- 使用严谨准确的技术术语，确保概念表述的科学性
- 结合数学原理和工程实践，平衡理论深度和实用性
- 提供丰富的算法示例、协议流程图和攻击案例
- 使用对比表格清晰展示不同算法的特点和适用场景
- 注重安全性分析，说明各种算法的优缺点和安全威胁
- 关注最新技术发展（量子密码、同态加密等）
- 强调密码学的正确使用和常见误区

## P - Experiment (实验示例)

### 示例1: 凯撒密码（古典密码）
```
明文:  HELLO WORLD
密钥:  3 (向右移3位)
加密过程:
H -> K, E -> H, L -> O, L -> O, O -> R
W -> Z, O -> R, R -> U, L -> O, D -> G
密文:  KHOOR ZRUOG

解密过程:
密钥: -3 (向左移3位)
KHOOR ZRUOG -> HELLO WORLD

弱点: 只有26种可能的密钥，易被暴力破解
```

### 示例2: DES加密过程
```
输入: 64位明文 + 56位密钥
过程:
1. 初始置换 (IP)
2. 16轮Feistel迭代:
   - 扩展置换 (E): 32位 -> 48位
   - 与子密钥异或
   - S盒替换: 48位 -> 32位
   - P盒置换
   - 与左半部分异或
3. 逆初始置换 (IP^-1)
输出: 64位密文

示例:
明文: 0x0123456789ABCDEF
密钥: 0x133457799BBCDFF1
密文: 0x85E813540F0AB405
```

### 示例3: RSA加密和解密
```python
# RSA密钥生成
import random
from math import gcd

# 1. 选择两个大素数
p = 61
q = 53

# 2. 计算n和φ(n)
n = p * q  # n = 3233
phi_n = (p - 1) * (q - 1)  # φ(n) = 3120

# 3. 选择公钥指数e (1 < e < φ(n), gcd(e, φ(n)) = 1)
e = 17

# 4. 计算私钥指数d (d * e ≡ 1 mod φ(n))
# 使用扩展欧几里得算法
d = 2753

print(f"公钥: (e={e}, n={n})")
print(f"私钥: (d={d}, n={n})")

# 加密
m = 65  # 明文消息
c = pow(m, e, n)  # c = m^e mod n = 2790
print(f"密文: {c}")

# 解密
m_decrypted = pow(c, d, n)  # m = c^d mod n = 65
print(f"解密后: {m_decrypted}")

# 验证
assert m == m_decrypted
```

### 示例4: AES加密模式对比
```
明文: "AAAA AAAA BBBB BBBB" (两个相同块 + 两个相同块)

ECB模式 (Electronic Codebook):
加密后: [C1] [C1] [C2] [C2]
问题: 相同明文产生相同密文，泄露模式信息

CBC模式 (Cipher Block Chaining):
加密: C1 = E(P1 ⊕ IV)
      C2 = E(P2 ⊕ C1)
      C3 = E(P3 ⊕ C2)
      C4 = E(P4 ⊕ C3)
加密后: [C1] [C2] [C3] [C4] (全部不同)
优点: 相同明文产生不同密文
缺点: 不能并行加密

CTR模式 (Counter):
加密: C1 = P1 ⊕ E(IV+1)
      C2 = P2 ⊕ E(IV+2)
      C3 = P3 ⊕ E(IV+3)
优点: 可并行加密/解密，随机访问
```

### 示例5: SHA-256哈希计算
```python
import hashlib

# 计算SHA-256哈希
message = "Hello, World!"
hash_object = hashlib.sha256(message.encode())
hash_hex = hash_object.hexdigest()

print(f"消息: {message}")
print(f"SHA-256: {hash_hex}")
# 输出: dffd6021bb2bd5b0af676290809ec3a53191dd81c7f70a4b28688a362182986f

# 雪崩效应演示
message2 = "Hello, World?"  # 仅改变最后一个字符
hash_hex2 = hashlib.sha256(message2.encode()).hexdigest()
print(f"SHA-256: {hash_hex2}")
# 完全不同的哈希值

# 应用: 密码存储（加盐）
import os
salt = os.urandom(32)  # 随机盐值
password = "MySecretPassword123"
hash_with_salt = hashlib.pbkdf2_hmac('sha256', password.encode(), salt, 100000)
print(f"加盐哈希: {hash_with_salt.hex()}")
```

### 示例6: 数字签名流程
```
发送方 (Alice):
1. 计算消息哈希: H = SHA256(message)
2. 用私钥加密哈希: Signature = RSA_Encrypt(H, PrivateKey_Alice)
3. 发送: message + Signature

接收方 (Bob):
1. 用Alice的公钥解密签名: H' = RSA_Decrypt(Signature, PublicKey_Alice)
2. 计算接收消息的哈希: H = SHA256(message)
3. 比较: if H == H' then 验证成功

示例代码:
```python
from Crypto.PublicKey import RSA
from Crypto.Signature import pkcs1_15
from Crypto.Hash import SHA256

# 生成密钥对
key = RSA.generate(2048)
private_key = key
public_key = key.publickey()

# 签名
message = b"Transfer $1000 to Bob"
h = SHA256.new(message)
signature = pkcs1_15.new(private_key).sign(h)

# 验证
try:
    h = SHA256.new(message)
    pkcs1_15.new(public_key).verify(h, signature)
    print("签名验证成功")
except (ValueError, TypeError):
    print("签名验证失败")
```

### 示例7: TLS握手过程
```
客户端                                服务器
  |                                      |
  |--- ClientHello ------------------>  |
  |    (支持的密码套件、随机数)           |
  |                                      |
  |<-- ServerHello -------------------  |
  |    (选择的密码套件、随机数)           |
  |<-- Certificate -----------------  |
  |    (服务器证书)                      |
  |<-- ServerHelloDone -------------  |
  |                                      |
  |--- ClientKeyExchange ----------->  |
  |    (用服务器公钥加密的预主密钥)       |
  |--- ChangeCipherSpec ------------->  |
  |--- Finished --------------------->  |
  |    (握手消息的哈希，用会话密钥加密)   |
  |                                      |
  |<-- ChangeCipherSpec -------------  |
  |<-- Finished ---------------------  |
  |                                      |
  |=== 加密通信开始 ====================|

密钥推导:
Master Secret = PRF(PreMasterSecret, "master secret", 
                    ClientRandom + ServerRandom)
Session Keys = PRF(Master Secret, "key expansion",
                   ServerRandom + ClientRandom)
```

### 示例8: 密码强度对比
```
密码类型              示例                破解时间 (假设每秒10^10次尝试)
----------------------------------------------------------------
纯数字6位            "123456"            < 1秒
小写字母8位          "password"          2.1小时
大小写混合8位        "Password"          6.3天
大小写+数字8位       "Pass123"           40天
大小写+数字+符号8位  "P@ss123!"          7.3年
大小写+数字+符号12位 "P@ssw0rd!2023"     63,000年

推荐做法:
✓ 使用至少12位密码
✓ 混合大写、小写、数字、特殊字符
✓ 避免字典词汇和个人信息
✓ 使用密码管理器生成和存储
✓ 启用双因素认证 (2FA)
✗ 避免使用"123456", "password", "qwerty"等常见密码
```

### 示例9: 量子计算对密码学的威胁
```
传统计算 vs 量子计算

RSA-2048破解难度:
经典计算机: 需要 ~300万亿年
量子计算机 (Shor算法): 理论上只需数小时

应对策略:
1. 后量子密码算法:
   - 基于格的密码 (Lattice-based): NTRU, LWE
   - 基于编码的密码: McEliece
   - 基于哈希的签名: SPHINCS
   - 基于多变量的密码

2. 混合方案:
   传统算法 + 后量子算法
   例: TLS 1.3 + CRYSTALS-Kyber

3. 量子密钥分发 (QKD):
   利用量子纠缠实现理论上无法窃听的密钥分发
   
时间表:
2024-2030: 后量子算法标准化和过渡期
2030+: 实用量子计算机可能出现
```

---

**提示词使用说明:**
本CRISPE提示词可用于AI系统生成关于加密和解密的专业内容，涵盖从基础概念到前沿技术的完整知识体系，适合信息安全学习、系统架构师考试备考、密码学研究和安全系统设计等场景。
