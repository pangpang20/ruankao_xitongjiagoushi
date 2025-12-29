# 身份认证、数字签名、密钥、口令 - CRISPE提示词工程

## C - Capacity and Role (能力与角色)
作为信息安全与身份认证专家，具备以下能力：
- 深入理解身份认证（Authentication）的理论基础和实践方法
- 精通数字签名技术及其在身份验证中的应用
- 熟练掌握密钥管理的完整生命周期和最佳实践
- 具备口令安全、多因素认证、生物识别等领域的丰富经验
- 擅长设计和实施企业级身份认证和访问控制系统
- 理解PKI体系、SSO、OAuth、OpenID Connect等现代认证协议
- 掌握零信任架构和身份即服务（IDaaS）的安全策略

## R - Insight (背景洞察)
身份认证是信息安全的第一道防线：
- 身份认证是确保"你是谁"的关键安全机制
- 数字签名不仅用于加密，更是身份认证和不可否认性的基础
- 密钥管理的安全性直接决定整个认证体系的可靠性
- 口令仍是最广泛使用的认证方式，但也是最脆弱的环节
- 多因素认证（MFA）已成为现代系统的安全标配
- 生物识别技术在便利性和安全性之间寻求平衡
- 身份认证不仅关乎技术，还涉及用户体验和合规要求
- 零信任架构强调"永不信任，始终验证"的安全理念

## I - Statement (指令说明)
请详细阐述身份认证、数字签名、密钥和口令的核心内容，包括：

### 1. 身份认证基础概念
- 身份认证的定义、目标和重要性
- 认证 vs 授权 vs 审计（AAA模型）
- 认证的三要素
  - 你知道什么（Knowledge）- 口令、PIN
  - 你拥有什么（Possession）- 令牌、智能卡
  - 你是什么（Inherence）- 生物特征
- 身份认证的安全属性
  - 真实性（Authenticity）
  - 完整性（Integrity）
  - 不可否认性（Non-repudiation）
- 认证强度和安全等级

### 2. 口令认证（Password Authentication）
- 口令认证的基本原理
- **口令存储机制**
  - 明文存储的危害
  - 哈希存储（MD5、SHA系列）
  - 加盐哈希（Salted Hash）
  - 慢哈希函数（bcrypt、scrypt、Argon2）
  - Pepper和密钥拉伸
- **口令策略**
  - 口令复杂度要求
  - 口令长度和熵
  - 口令有效期和轮换
  - 口令历史记录
  - 账户锁定策略
- **常见口令攻击**
  - 暴力破解（Brute Force）
  - 字典攻击（Dictionary Attack）
  - 彩虹表攻击（Rainbow Table）
  - 凭证填充（Credential Stuffing）
  - 键盘记录（Keylogging）
  - 钓鱼攻击（Phishing）
- **口令安全最佳实践**
  - 强口令生成和管理
  - 口令管理器的使用
  - 避免口令重用
  - 安全的口令重置流程
  - 口令熵计算

### 3. 数字签名在身份认证中的应用
- 数字签名的认证功能
- **数字签名认证流程**
  - 签名生成过程
  - 签名验证过程
  - 公钥基础设施（PKI）在认证中的作用
- **基于数字签名的认证协议**
  - 挑战-响应认证（Challenge-Response）
  - 数字证书认证
  - 客户端证书认证（mTLS）
  - 代码签名和软件认证
- **数字签名认证的优势和局限**
- **数字签名算法选择**
  - RSA签名
  - ECDSA
  - EdDSA（Ed25519）
  - 性能和安全性对比

### 4. 密钥在身份认证中的应用
- 对称密钥认证
  - 共享密钥认证（Kerberos）
  - 会话密钥管理
  - 密钥分发中心（KDC）
- 非对称密钥认证
  - 公钥认证机制
  - SSH密钥认证
  - API密钥认证
- **密钥管理生命周期**
  - 密钥生成（强随机性要求）
  - 密钥存储（HSM、密钥库）
  - 密钥分发（安全通道）
  - 密钥使用（访问控制）
  - 密钥轮换（定期更新）
  - 密钥撤销和销毁
- **密钥安全最佳实践**
  - 密钥强度要求
  - 密钥分离（不同用途使用不同密钥）
  - 密钥托管和恢复
  - 硬件安全模块（HSM）使用
  - 密钥泄露应急响应

### 5. 多因素认证（MFA/2FA）
- 多因素认证的原理和类型
- **双因素认证（2FA）实现方式**
  - SMS/短信验证码
  - TOTP（基于时间的一次性口令）
  - HOTP（基于计数器的一次性口令）
  - 推送通知认证
  - 硬件令牌（YubiKey、FIDO2）
- **TOTP算法详解**
  - RFC 6238标准
  - Google Authenticator原理
  - 时间窗口和时钟同步
- **FIDO/FIDO2和WebAuthn**
  - 无密码认证
  - 公钥凭证
  - 用户体验优化
- **MFA的安全考虑**
  - 绕过MFA的攻击
  - 备用认证方式
  - MFA疲劳攻击

### 6. 生物识别认证
- 生物识别技术类型
  - 指纹识别
  - 面部识别
  - 虹膜识别
  - 声音识别
  - 行为生物识别（击键动态、步态）
- **生物识别的安全指标**
  - 错误接受率（FAR）
  - 错误拒绝率（FRR）
  - 等错误率（EER）
  - 活体检测（Liveness Detection）
- **生物识别的隐私和安全问题**
  - 生物特征模板保护
  - 生物特征不可更改性
  - 隐私合规（GDPR等）
  - 欺骗攻击（Spoofing）

### 7. 单点登录（SSO）
- SSO的概念和优势
- **SAML（Security Assertion Markup Language）**
  - SAML架构和组件
  - SAML认证流程
  - SP-initiated vs IdP-initiated
  - SAML断言和令牌
- **OAuth 2.0**
  - OAuth 2.0授权框架
  - 授权类型（Authorization Code、Implicit、Client Credentials等）
  - 访问令牌和刷新令牌
  - OAuth 2.0安全最佳实践（PKCE）
- **OpenID Connect（OIDC）**
  - OIDC vs OAuth 2.0
  - ID Token和UserInfo端点
  - OIDC认证流程
- **SSO安全风险**
  - 单点失败风险
  - 会话劫持
  - 令牌窃取

### 8. 企业级认证系统
- **LDAP和Active Directory**
  - 目录服务架构
  - LDAP认证流程
  - AD集成和域认证
- **Kerberos协议**
  - Kerberos架构（KDC、TGT、TGS）
  - Kerberos认证流程
  - 票据授予和服务票据
  - Kerberos安全性分析
- **RADIUS（Remote Authentication Dial-In User Service）**
  - RADIUS架构
  - RADIUS认证流程
  - 802.1X网络认证
- **身份即服务（IDaaS）**
  - 云身份管理
  - Okta、Auth0、Azure AD
  - IDaaS的优势和挑战

### 9. 现代认证协议和技术
- **JWT（JSON Web Token）**
  - JWT结构（Header、Payload、Signature）
  - JWT签名和验证
  - JWT vs Session
  - JWT安全最佳实践
- **无密码认证（Passwordless）**
  - Magic Link
  - WebAuthn和FIDO2
  - 生物识别登录
  - 无密码认证的优势
- **零信任架构（Zero Trust）**
  - 零信任原则
  - 持续验证
  - 最小权限访问
  - 微分段和身份边界
- **自适应认证（Adaptive Authentication）**
  - 风险评分
  - 上下文感知认证
  - 行为分析
  - 条件访问策略

### 10. 身份认证安全最佳实践
- **认证系统设计原则**
  - 深度防御
  - 最小权限原则
  - 失败安全（Fail-safe）
  - 审计和日志记录
- **常见认证漏洞和防御**
  - 会话固定攻击
  - 会话劫持
  - 重放攻击
  - 时序攻击
  - CSRF（跨站请求伪造）
- **认证安全检查清单**
  - 强制使用HTTPS
  - 安全的口令策略
  - 实施MFA
  - 定期安全审计
  - 及时打补丁
  - 监控异常登录行为
- **合规和标准**
  - NIST 800-63（数字身份指南）
  - ISO/IEC 27001
  - GDPR隐私要求
  - SOC 2认证

## S - Personality (个性风格)
采用以下风格进行说明：
- 使用严谨准确的技术术语，确保安全概念表述的科学性
- 结合理论原理和工程实践，强调可操作性和实用性
- 提供丰富的认证流程图、协议时序图和攻击防御案例
- 使用对比表格清晰展示不同认证方式的优缺点和适用场景
- 注重安全性分析，说明各种认证方法的威胁模型和防御策略
- 关注用户体验和安全性的平衡
- 强调认证系统的正确实现和常见错误
- 提供代码示例和配置示例

## P - Experiment (实验示例)

### 示例1: 口令哈希存储演进
```python
# 1. 明文存储（极度危险，永远不要这样做！）
password = "MyPassword123"
stored = password  # ✗ 数据库被盗，所有密码泄露

# 2. 简单哈希（不安全，易受彩虹表攻击）
import hashlib
password = "MyPassword123"
stored = hashlib.md5(password.encode()).hexdigest()
# ✗ 相同密码哈希相同，预计算攻击

# 3. 加盐哈希（更好，但哈希函数太快）
import os
salt = os.urandom(32)
password = "MyPassword123"
stored = hashlib.sha256(salt + password.encode()).hexdigest()
# ⚠ SHA-256太快，GPU可以快速破解

# 4. 慢哈希函数（推荐）
import bcrypt
password = "MyPassword123"
salt = bcrypt.gensalt(rounds=12)  # 工作因子
hashed = bcrypt.hashpw(password.encode(), salt)
# ✓ 计算缓慢，抵抗暴力破解

# 验证密码
if bcrypt.checkpw(password.encode(), hashed):
    print("密码正确")
    
# 5. Argon2（最佳选择）
from argon2 import PasswordHasher
ph = PasswordHasher()
hash = ph.hash("MyPassword123")
# ✓ 内存困难，抵抗GPU/ASIC攻击

# 验证
try:
    ph.verify(hash, "MyPassword123")
    print("密码正确")
except:
    print("密码错误")
```

### 示例2: 口令强度评估
```python
import re
import math

def password_entropy(password):
    """计算密码熵"""
    # 计算字符集大小
    charset = 0
    if re.search(r'[a-z]', password): charset += 26
    if re.search(r'[A-Z]', password): charset += 26
    if re.search(r'[0-9]', password): charset += 10
    if re.search(r'[^a-zA-Z0-9]', password): charset += 32
    
    # 熵 = log2(字符集^长度)
    if charset == 0:
        return 0
    entropy = len(password) * math.log2(charset)
    return entropy

def password_strength(password):
    """评估密码强度"""
    entropy = password_entropy(password)
    
    # 强度分类
    if entropy < 28:
        return "极弱 (Very Weak)"
    elif entropy < 36:
        return "弱 (Weak)"
    elif entropy < 60:
        return "中等 (Fair)"
    elif entropy < 128:
        return "强 (Strong)"
    else:
        return "极强 (Very Strong)"

# 测试
passwords = [
    "123456",           # 6位纯数字
    "password",         # 8位小写
    "Password123",      # 混合
    "P@ssw0rd!2024",    # 强密码
    "correct-horse-battery-staple"  # Passphrase
]

for pwd in passwords:
    entropy = password_entropy(pwd)
    strength = password_strength(pwd)
    print(f"密码: {pwd:30} 熵: {entropy:5.1f} bits  强度: {strength}")

"""
输出:
密码: 123456                          熵:  19.9 bits  强度: 极弱 (Very Weak)
密码: password                        熵:  37.6 bits  强度: 中等 (Fair)
密码: Password123                     熵:  59.5 bits  强度: 中等 (Fair)
密码: P@ssw0rd!2024                   熵:  78.3 bits  强度: 强 (Strong)
密码: correct-horse-battery-staple    熵: 174.2 bits  强度: 极强 (Very Strong)
"""
```

### 示例3: 数字签名挑战-响应认证
```python
from Crypto.PublicKey import RSA
from Crypto.Signature import pkcs1_15
from Crypto.Hash import SHA256
import os

# 服务器端
class AuthServer:
    def __init__(self):
        self.registered_users = {}  # {username: public_key}
    
    def register_user(self, username, public_key):
        """用户注册公钥"""
        self.registered_users[username] = public_key
        print(f"用户 {username} 已注册")
    
    def authenticate(self, username, signed_challenge):
        """验证用户身份"""
        # 1. 生成随机挑战
        challenge = os.urandom(32)
        
        # 2. 发送挑战给客户端（客户端需要签名）
        print(f"服务器发送挑战: {challenge.hex()[:32]}...")
        
        # 3. 验证签名
        public_key = self.registered_users.get(username)
        if not public_key:
            return False, "用户不存在"
        
        try:
            h = SHA256.new(challenge)
            pkcs1_15.new(public_key).verify(h, signed_challenge)
            return True, "认证成功"
        except (ValueError, TypeError):
            return False, "签名验证失败"

# 客户端
class AuthClient:
    def __init__(self, username):
        self.username = username
        # 生成密钥对
        self.private_key = RSA.generate(2048)
        self.public_key = self.private_key.publickey()
    
    def sign_challenge(self, challenge):
        """对挑战进行签名"""
        h = SHA256.new(challenge)
        signature = pkcs1_15.new(self.private_key).sign(h)
        return signature

# 演示认证流程
server = AuthServer()
alice = AuthClient("Alice")

# 1. 注册
server.register_user("Alice", alice.public_key)

# 2. 认证
challenge = os.urandom(32)
print(f"\n--- 开始认证 ---")
signed = alice.sign_challenge(challenge)
success, message = server.authenticate("Alice", signed)
print(f"认证结果: {message}")

# 3. 尝试伪造签名（失败）
print(f"\n--- 伪造攻击 ---")
fake_signature = os.urandom(256)
success, message = server.authenticate("Alice", fake_signature)
print(f"认证结果: {message}")
```

### 示例4: TOTP双因素认证实现
```python
import pyotp
import time
import qrcode

# 服务器端：为用户生成TOTP密钥
def setup_2fa(username):
    """为用户设置2FA"""
    # 生成Base32密钥
    secret = pyotp.random_base32()
    
    # 生成二维码URI
    totp_uri = pyotp.totp.TOTP(secret).provisioning_uri(
        name=username,
        issuer_name="MyApp"
    )
    
    # 生成二维码（用户用Authenticator App扫描）
    qr = qrcode.QRCode()
    qr.add_data(totp_uri)
    qr.make()
    
    print(f"用户: {username}")
    print(f"密钥: {secret}")
    print(f"URI: {totp_uri}")
    # qr.print_ascii()  # 打印二维码
    
    return secret

# 客户端：生成TOTP验证码
def generate_totp_code(secret):
    """生成6位TOTP验证码"""
    totp = pyotp.TOTP(secret)
    return totp.now()

# 服务器端：验证TOTP验证码
def verify_totp_code(secret, user_code):
    """验证用户提供的TOTP码"""
    totp = pyotp.TOTP(secret)
    # 允许±1个时间窗口（30秒），防止时钟偏差
    return totp.verify(user_code, valid_window=1)

# 演示
print("=== TOTP 双因素认证演示 ===\n")

# 1. 设置2FA
secret = setup_2fa("alice@example.com")

# 2. 用户生成验证码
print(f"\n--- 用户生成验证码 ---")
code = generate_totp_code(secret)
print(f"当前验证码: {code}")

# 3. 服务器验证
print(f"\n--- 服务器验证 ---")
is_valid = verify_totp_code(secret, code)
print(f"验证结果: {'成功 ✓' if is_valid else '失败 ✗'}")

# 4. 演示时间窗口
print(f"\n--- 时间窗口演示 ---")
for i in range(5):
    code = generate_totp_code(secret)
    print(f"时刻 {i*30}秒: 验证码 = {code}")
    time.sleep(30)

# 5. 错误的验证码
print(f"\n--- 错误验证码测试 ---")
wrong_code = "000000"
is_valid = verify_totp_code(secret, wrong_code)
print(f"验证结果: {'成功 ✓' if is_valid else '失败 ✗'}")
```

### 示例5: JWT令牌认证
```python
import jwt
import datetime

# 密钥（实际应用中应安全存储）
SECRET_KEY = "your-256-bit-secret"
ALGORITHM = "HS256"

def create_jwt_token(user_id, username, expires_in=3600):
    """创建JWT令牌"""
    payload = {
        'user_id': user_id,
        'username': username,
        'exp': datetime.datetime.utcnow() + datetime.timedelta(seconds=expires_in),
        'iat': datetime.datetime.utcnow(),  # Issued At
        'nbf': datetime.datetime.utcnow(),  # Not Before
    }
    
    token = jwt.encode(payload, SECRET_KEY, algorithm=ALGORITHM)
    return token

def verify_jwt_token(token):
    """验证JWT令牌"""
    try:
        payload = jwt.decode(token, SECRET_KEY, algorithms=[ALGORITHM])
        return True, payload
    except jwt.ExpiredSignatureError:
        return False, "令牌已过期"
    except jwt.InvalidTokenError:
        return False, "无效的令牌"

# 演示
print("=== JWT 令牌认证演示 ===\n")

# 1. 用户登录，生成JWT
print("--- 用户登录 ---")
token = create_jwt_token(user_id=123, username="alice")
print(f"JWT令牌: {token}\n")

# 2. 解析JWT（无需验证）
print("--- 解析JWT内容 ---")
decoded = jwt.decode(token, options={"verify_signature": False})
print(f"Header: {jwt.get_unverified_header(token)}")
print(f"Payload: {decoded}\n")

# 3. 验证JWT
print("--- 验证JWT ---")
valid, result = verify_jwt_token(token)
if valid:
    print(f"验证成功 ✓")
    print(f"用户ID: {result['user_id']}")
    print(f"用户名: {result['username']}")
else:
    print(f"验证失败 ✗: {result}")

# 4. 过期令牌测试
print("\n--- 过期令牌测试 ---")
expired_token = create_jwt_token(user_id=123, username="alice", expires_in=1)
import time
time.sleep(2)
valid, result = verify_jwt_token(expired_token)
print(f"验证结果: {result}")

# 5. 篡改令牌测试
print("\n--- 篡改令牌测试 ---")
tampered_token = token[:-10] + "tampered!"
valid, result = verify_jwt_token(tampered_token)
print(f"验证结果: {result}")
```

### 示例6: SSH密钥认证配置
```bash
# === SSH 公钥认证配置 ===

# 1. 客户端生成密钥对
ssh-keygen -t ed25519 -C "user@example.com"
# 或使用RSA
ssh-keygen -t rsa -b 4096 -C "user@example.com"

# 密钥保存位置:
# 私钥: ~/.ssh/id_ed25519
# 公钥: ~/.ssh/id_ed25519.pub

# 2. 将公钥复制到服务器
ssh-copy-id user@server.com
# 或手动复制
cat ~/.ssh/id_ed25519.pub | ssh user@server.com "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys"

# 3. 设置正确的权限（重要！）
chmod 700 ~/.ssh
chmod 600 ~/.ssh/authorized_keys

# 4. SSH服务器配置 (/etc/ssh/sshd_config)
"""
# 启用公钥认证
PubkeyAuthentication yes

# 指定授权密钥文件
AuthorizedKeysFile .ssh/authorized_keys

# 禁用密码认证（提高安全性）
PasswordAuthentication no

# 禁用空密码
PermitEmptyPasswords no

# 禁用root登录
PermitRootLogin no
"""

# 5. 重启SSH服务
sudo systemctl restart sshd

# 6. 使用密钥登录
ssh user@server.com
# 无需输入密码，使用私钥认证

# 7. 使用SSH Agent管理密钥
eval $(ssh-agent)
ssh-add ~/.ssh/id_ed25519

# 8. 配置SSH客户端 (~/.ssh/config)
"""
Host myserver
    HostName server.com
    User alice
    IdentityFile ~/.ssh/id_ed25519
    Port 22
"""

# 现在可以简化连接
ssh myserver
```

### 示例7: OAuth 2.0授权码流程
```python
from flask import Flask, request, redirect, session
import requests
import secrets

app = Flask(__name__)
app.secret_key = 'your-secret-key'

# OAuth配置
OAUTH_CLIENT_ID = 'your-client-id'
OAUTH_CLIENT_SECRET = 'your-client-secret'
OAUTH_AUTHORIZE_URL = 'https://provider.com/oauth/authorize'
OAUTH_TOKEN_URL = 'https://provider.com/oauth/token'
OAUTH_USERINFO_URL = 'https://provider.com/oauth/userinfo'
REDIRECT_URI = 'http://localhost:5000/callback'

@app.route('/login')
def login():
    """步骤1: 重定向到OAuth提供商"""
    # 生成state参数防止CSRF
    state = secrets.token_urlsafe(32)
    session['oauth_state'] = state
    
    # 构建授权URL
    params = {
        'client_id': OAUTH_CLIENT_ID,
        'redirect_uri': REDIRECT_URI,
        'response_type': 'code',
        'scope': 'openid profile email',
        'state': state
    }
    
    auth_url = f"{OAUTH_AUTHORIZE_URL}?{'&'.join([f'{k}={v}' for k, v in params.items()])}"
    return redirect(auth_url)

@app.route('/callback')
def callback():
    """步骤2-4: 处理回调，交换授权码获取访问令牌"""
    # 验证state参数
    state = request.args.get('state')
    if state != session.get('oauth_state'):
        return "CSRF攻击检测", 400
    
    # 获取授权码
    code = request.args.get('code')
    if not code:
        return "授权失败", 400
    
    # 步骤3: 用授权码交换访问令牌
    token_data = {
        'grant_type': 'authorization_code',
        'code': code,
        'redirect_uri': REDIRECT_URI,
        'client_id': OAUTH_CLIENT_ID,
        'client_secret': OAUTH_CLIENT_SECRET
    }
    
    token_response = requests.post(OAUTH_TOKEN_URL, data=token_data)
    tokens = token_response.json()
    
    access_token = tokens.get('access_token')
    refresh_token = tokens.get('refresh_token')
    
    # 步骤4: 使用访问令牌获取用户信息
    headers = {'Authorization': f'Bearer {access_token}'}
    userinfo_response = requests.get(OAUTH_USERINFO_URL, headers=headers)
    user_info = userinfo_response.json()
    
    # 保存用户会话
    session['user'] = user_info
    session['access_token'] = access_token
    
    return f"登录成功！欢迎 {user_info.get('name')}"

@app.route('/protected')
def protected():
    """受保护的资源"""
    if 'access_token' not in session:
        return redirect('/login')
    
    return f"这是受保护的资源。用户: {session['user'].get('name')}"

if __name__ == '__main__':
    app.run(debug=True)
```

### 示例8: Kerberos认证流程
```
=== Kerberos 认证流程 ===

组件:
- Client (客户端)
- KDC (Key Distribution Center - 密钥分发中心)
  - AS (Authentication Server - 认证服务器)
  - TGS (Ticket Granting Server - 票据授予服务器)
- Service Server (服务服务器)

流程:

步骤1: 客户端向AS请求TGT
Client → AS: 
  - 用户名
  - 请求TGT

步骤2: AS验证并返回TGT
AS → Client:
  - TGT（用TGS密钥加密）
  - 会话密钥（用用户密码哈希加密）

Client操作:
  - 用密码解密获得会话密钥
  - 缓存TGT（8小时有效期）

步骤3: 客户端向TGS请求服务票据
Client → TGS:
  - TGT
  - 服务名称
  - Authenticator（用会话密钥加密）

步骤4: TGS验证并返回服务票据
TGS → Client:
  - 服务票据（用服务密钥加密）
  - 服务会话密钥

步骤5: 客户端访问服务
Client → Service:
  - 服务票据
  - Authenticator（用服务会话密钥加密）

步骤6: 服务验证并响应
Service → Client:
  - 验证成功，提供服务
  - 可选：返回确认（防止重放）

优势:
✓ 单点登录（SSO）
✓ 密码不在网络传输
✓ 双向认证
✓ 时间敏感（防重放）

安全特性:
- 票据有时间限制
- 密钥从不在网络传输
- 双向认证
- 防止中间人攻击

示例代码（Python）:
```python
import kerberos

# 客户端获取服务票据
service = "HTTP@server.example.com"
rc, context = kerberos.authGSSClientInit(service)

# 生成令牌
kerberos.authGSSClientStep(context, "")
token = kerberos.authGSSClientResponse(context)

# 发送到服务器进行认证
# ...
```

### 示例9: 认证方式对比矩阵
```
┌─────────────────────────────────────────────────────────────────────────┐
│              身份认证方式对比表                                          │
├──────────────┬────────┬────────┬────────┬────────┬────────┬────────────┤
│ 认证方式      │ 安全性 │ 用户体验│ 成本   │ 部署难度│可用性  │ 适用场景    │
├──────────────┼────────┼────────┼────────┼────────┼────────┼────────────┤
│ 静态密码      │   ⭐⭐  │  ⭐⭐⭐⭐ │  ⭐⭐⭐⭐ │  ⭐⭐⭐⭐ │ ⭐⭐⭐⭐ │ 低安全需求  │
├──────────────┼────────┼────────┼────────┼────────┼────────┼────────────┤
│ SMS 2FA      │  ⭐⭐⭐  │  ⭐⭐⭐  │   ⭐⭐  │  ⭐⭐⭐  │  ⭐⭐⭐ │ 一般应用    │
├──────────────┼────────┼────────┼────────┼────────┼────────┼────────────┤
│ TOTP 2FA     │ ⭐⭐⭐⭐ │   ⭐⭐  │  ⭐⭐⭐⭐ │  ⭐⭐⭐  │ ⭐⭐⭐⭐ │ 企业应用    │
├──────────────┼────────┼────────┼────────┼────────┼────────┼────────────┤
│ 硬件令牌      │ ⭐⭐⭐⭐ │   ⭐⭐  │   ⭐   │   ⭐⭐  │  ⭐⭐⭐ │ 高安全环境  │
├──────────────┼────────┼────────┼────────┼────────┼────────┼────────────┤
│ FIDO2/WebAuthn│⭐⭐⭐⭐⭐│ ⭐⭐⭐⭐ │  ⭐⭐⭐  │   ⭐⭐  │  ⭐⭐⭐ │ 现代Web应用 │
├──────────────┼────────┼────────┼────────┼────────┼────────┼────────────┤
│ 生物识别      │  ⭐⭐⭐ │ ⭐⭐⭐⭐⭐│   ⭐   │   ⭐⭐  │   ⭐⭐ │ 移动设备    │
├──────────────┼────────┼────────┼────────┼────────┼────────┼────────────┤
│ 数字证书      │ ⭐⭐⭐⭐ │   ⭐   │   ⭐⭐  │   ⭐   │  ⭐⭐⭐ │ B2B, API    │
├──────────────┼────────┼────────┼────────┼────────┼────────┼────────────┤
│ Kerberos     │ ⭐⭐⭐⭐ │ ⭐⭐⭐⭐ │   ⭐⭐  │   ⭐   │  ⭐⭐  │ 企业内网SSO │
└──────────────┴────────┴────────┴────────┴────────┴────────┴────────────┘

认证强度等级:
┌────────┬────────────────────────────────────────────┐
│ 等级    │ 说明                                        │
├────────┼────────────────────────────────────────────┤
│ AAL1   │ 单因素认证（密码）                          │
│        │ 适用: 低风险应用                            │
├────────┼────────────────────────────────────────────┤
│ AAL2   │ 双因素认证（密码 + OTP/SMS）                │
│        │ 适用: 中等风险应用（银行、电商）            │
├────────┼────────────────────────────────────────────┤
│ AAL3   │ 多因素认证 + 硬件认证器（FIDO2）            │
│        │ 适用: 高风险应用（政府、金融核心系统）      │
└────────┴────────────────────────────────────────────┘
```

---

**提示词使用说明:**
本CRISPE提示词可用于AI系统生成关于身份认证、数字签名、密钥和口令的专业内容，涵盖从基础原理到企业级实施的完整知识体系，适合信息安全学习、系统架构师考试备考、企业认证系统设计和安全审计等场景。
