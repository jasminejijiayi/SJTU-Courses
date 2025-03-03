cryptography

区块链就是去中心化的数据库

the study of secure communication over insecure channels

provide rigorous guarantees on the security of data and computation in the presence of an attacker

人都不可信，唯一相信的是数学，在图灵之前的时代，都是艺术的脑子一拍进行bug-attack-fix 

如今除非数学被破解，否则难以破解密码

goal：

1. read -- confidentiality
2. write -- Integrity
3. Authenticity -- identical certification



key：

1. Symmetric key model 元数据（辅助算法运算数据）
2. Asymmetric key model（Secret key & Public key）



Security Principle： Kerckhoff’s Principle

攻击者可以知道算法流程，但不知道密钥key的输入，知道的是Lock和Unlock的算法







confidentiality

Plaintext

Ciphertext





Integrity & Authenticity

Seal 字符串 Tag

Create - Seal - Check



Threat Models

量子计算机还未出现之前

Chosen-plaintext 







Cryptography Roadmap

对称密钥加密（保护读的信息）

Symmetric-Key Encryption

1. KeyGen()

2. Enc()

3. Dec()



cannot read: 看到字符串的先验信息是否等于后验信息



A plaintext attack 明文攻击

IND-CPA

如何破解确定性算法？ easy

game消除了确定性算法，一定得加入随机数才有可能是安全的



Diffie-Hellman Key Exchange

MSG:加密加密解密解密（小马过河）



Discrete Log Problem and Diffle-Hellman Problem

Security: 中间人



Public-Key Encryption

1. KeyGen()
2. Enc(PK,M)
3. Dec(SK,C)



Properity

