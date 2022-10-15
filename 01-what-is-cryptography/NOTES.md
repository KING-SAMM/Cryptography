WHAT IS CRYPTOGRAPHY?
------------------------------------------
```
Cryptography is the science of encrypting and decrypting information to prevent unauthorized access.

The decryptiion process should be known to both the sender and the receiver
```

HOW DOES CRYPTOGRAPHY WORK?
ENCRYPTION AND DECRYPTION
------------------------------------------
```
Encryption is a primary route of employing cryptograohy by adding certain algorithms to jumble up the data.

Decryption is the process of reversing the work done by encrypting information so that the data becomes readable again

Both methods form the basis of cryptotgraphy
```

CIPHERS, PLAINTEXT AND CIPHERTEXT
------------------------------------------
```
Cipher      - An algorithm for encrypting data. It is a set of detailed steps to be carried out one after the other to make sure that the data becomes as unreadable as possible until it reaches the receiver.
Plaintext   - Data before encryption (or after decryption)
Ciphertext  - Data after encryption
Encryption Key  - Key used to scramble the data

```

APPLICATIONS OF CRYPTOGRAPHY
------------------------------------------
```
1. SSL/TLS
2. Digital Signatures
3. Safe Online Banking
4. Secure Chatting Services
5. Encrypted Emails
6. Crypto-currency
```

TYPES OF ENCRYPTION IN CRYPTOGRAPHY
------------------------------------------
```
1. Symmetric Key Cryptography
2. Asymmetric Key Cryptography
```

SYMMETRIC KEY CRYPTOGRAPHY
------------------------------------------
```
Symmetric key Cryptography relies on a single key for encrypting and decrypting the information. The key needs to be kept secret and be available to both the sender and receiver. Strength of encryption depends on the key size being used.

The secret key should not be sent along with the cipher text to the receiver.
Key exchange can be done beefore hand using other algorithms.
```

APPLICATIONS OF SYMMETRIC KEY CRYPTOGRAPHY
------------------------------------------
```
1. Banking applications to authenticate ID and transctions
2. Server/Data Center information can be encrypted at rest
3. HTTPS encryption with secure all-around browsing
```

DISADVANTAGES OF SYMMETRIC KEY CRYPTOGRAPHY
------------------------------------------
```
1. Same key for encryption and decryption means single point of failure.
2. Key needs to be always kept secret.
3. Receiver / Third party can also generate messages with the same key, so authentication issue will arise should secret key is leaked.
```

ADVANTAGES OF SYMMETRIC KEY CRYPTOGRAPHY
------------------------------------------
```
1. Faster than Asymmetric.
2. Better performance metrics.
3. Optimized for bulk amounts of data
4. Easier to set up and implement
```


PRIVATE-KEY CRYPTOGRAPHY VS PUBLIC-KEY CRYPTOGRAPHY
------------------------------------------
```
Symmetric key cryptography is also termed Private-Key Cryptography since a big part of the data's integrity is riding on the promise that the users can keep the key secret.

Asymmetric key cryptography is termed public key cryptography because it has two different keys at play, one of which is public.
```

TYPES OF ENCRYTION IN SYMMETERIC KEY CRYPTOGRAPHY
------------------------------------------
```
1. Stream Ciphers
2. Block Ciphers
```

STREAM CIPHERS
------------------------------------------
```
Stream ciphers are the algorithms that encrypt basic information one bit/byte at a time.

Features:
1. Encrytion is done one bit/byte at a time
2. Quicker format of encryption
3. Data is converted to binary digits and encrypted sequentially
4. Popular algorithms are RC4, Salsa20
```


BLOCK CIPHERS
------------------------------------------
```
Block ciphers are the algorithms that break down information into chunks of fixed size and encrypt those chunks/blocks.

Features:
1. Infromation is broken down into chunks/blocks of fixed size.
2. Size of block depends on key size or exact cipher used e.g a 128-bit block cipher will break the plain text into blocks of 128 bits eack, and encrypt those blocks instead of a single digit
3. The chunks are encrypted and later chained together
4. Popular algorithms are AES, DES, 3DES

Block ciphers are slower, but they are more tamper proof.
```

ASYMMETRIC KEY CRYPTOGRAPHY
------------------------------------------
```
Asymmetric Key Cryptography is a cryptographic method which uses two different keys for encryption and decryption. The key used for encryption is the public key while the key used for decryption is the private key.

The pair of keys must belong to the receiver of the message.
```


APPLICATIONS OF ASYMMETRIC KEY CRYPTOGRAPHY
------------------------------------------
```
1. Digital signatures to maintain authenticity of documents.
2. Managing crypto-currency transactions securely.
3. Encryptd browsing sessions for better protection against hackers.
4. Sharing keys for symmetric key cryptography.
```

ADVANTAGES OF ASYMMETRIC OVER SYMMETRIC KEY CRYPTOGRAPHY
------------------------------------------
```
1. No need for sharng secret keys - the key that can be shared cannot decrypt any information, and the only key that can decrypt doesn't need to be shared.
2. Longer key lenghts mean stronger encryption.
3. proof of owner's authenticity.
4. Data can't be modified.
```


