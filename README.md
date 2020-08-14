# iOSCrypto
This is a iOS crypto library. It supports following functions:
- [x] Symmetry Cipher
- [ ] Asymmetry Cipher
- [ ] Hashing function
## Symmetry Cipher
### Implement a Symmetric Cipher

```swift
let alghrithm: SymmetryCipher.Algorithm = .aes
let data = "Hello world".data(using: .utf8)!
// Generate random key
let key = try alghrithm.generateRandomKey()
// Generate random IV
let iv = alghrithm.generateRandomIV()
let cipher = try SymmetryCipher(algorithm: alghrithm, key: key, iv: iv)
// Encrypt data
let encrypted = try cipher.process(.encrypt, data: data)
// Decrypt data
let decrypted = try cipher.process(.decrypt, data: encrypted)
```

### Supported Symmetric algorithms
* AES
* DES
* Tripple DES
* Cast
* RC4
* RC2
* Blowfish

### Supported modes

* ECB
* CBC
* CFB
* CTR
* OFB
* RC4
* CFB8
