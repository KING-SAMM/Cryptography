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


HASHING
------------------------------------------
```
Hashing is the process of scrambling a piecce of information beyond recognition. They are designed to be irreversible. We pass the input through a hash function to calculate the 'Hash Value'. 'Hash' or 'Digest'
```


HASH FUNCTION
------------------------------------------
```
A hash function is an algorithm that performs Mathematical operations in the main plain text.

- A hash function is a set of Mathematical operations carried out on two blocks of data.
- Both blocks are created by dividing the initial input into equal parts
- The block size is dependent on the algorithm being used
- The digest size is dependent on the algorithm being used e.g MD5 has a digest size of 128 bits, SHA-256 a digest size of 256 bits
- Irreversible by design (NOTE: Some algorithms, like md5 have been compromised)
- Can be carried out multiple times, but the final digest must be consistent for the same input
```

REAL WORLD IMPLEMENTATION OF HASHING
------------------------------------------
```
1. Password Storage:
When a new user signs-up, the new password is passed through the hash function and the digest is stored on the server. 

When the same user tries to log-in, the password they input is passed through the function again and the digest is compared to the one stored on the servers.

If the re-calculated hash matches the hash stored on the servers during initial sign-up, the log-in is allowed.

If the re-calculated digest is different from the one on the server, the login is denied from the website.

2. Integrity Checks:
When a file is uploaded on the internet, the file's hash value is generated and it is uploaded along with the original information.

When a new user downloads the file, he can calculate the digest of the dowloaded file using the same hash function.

When the hash values are compared, if they match, then fiile integrity has been maintained and theren has been no data corruption.
```

HASHING GUIDELINES
------------------------------------------
```
1. The hash function must be fast, but not instantaneous
- Should be able to hash en-mass within a reasonable time limit to prevent exploitation
- Ultra quick algorithms can be tested vigorously for brute force attacks
- With enough brute force attacks, not just the hash, but the entire algorithm can be cracked

2. Hash digest must be dependent on each bit
- If a single character chages, a substamtial portion of the digest must change
- This is helpful in creating as many unique hashes as possible
- Hash digest for the plain text 'Cryptography' will be completely different from the plaintext 'Cryptograph 
```

HASH COLLISION
------------------------------------------
```
A hash collision occurs when there are two exact same hash values/digests resulting from two different users having the exact same password

- Since there is only one hash function for each server, same passwords have same digests after hashing

Hash collisions are more common than one would expect.
```

SALTING
------------------------------------------
```
Salting is the process of adding a random keyword to the end of the input before it is passed on to the hash function

- The random keyword added is called the 'salt value' or 'salt'
- The salt is unique forn each user in the database and is helpful to battle hash collisions.
```

PROBLEM WITH SALTING
------------------------------------------
```
Since the salt is unique for each user, they need to be stored in the database along with the passwords, and sometimes in plain text to speed up the process of continuous verification.

If the server is hacked, the passwords need to be brute forced which takes a lot of time, but if they received salts as well, the entire process becomes very fast
```

PEPPERING
------------------------------------------
```
Peppering is the process of adding the same random value at the end of a plaintext (input) before passing it to the hash function.

- It is NOT unique per user, and so the random value need not be stored on the server
- In the case of data breach, pepper value is safe from further exploitation

Many websites use a combination of salting and peppering to solve the problem of hash collisions as well as bolster security
```

SYMMETRIC ENCRYPTION: AES-256
------------------------------------------
```
The most widely used Symmetric Encryption algorithm today is the Advanced Encryption Standard (AES) which has a key size of 256 bit, with 128 bit and 196 bit key sizes also available.

Othe primitive algorithm like:
Data Encryption Standard (DES),
Triple Data Encryption Standard (3DES), and
64-bit Block Cipher (Blowfish)

all have fallen out of favour with the rise of AES
```

ORIGIN OF DES
------------------------------------------
```
DES is based on a feistel block cipher called Lucifer developed in 1971 by an IBM cryptography researcher, Horst Feistel. 

DES was approved as a standard in November 1976, and and later reaffirmed as a standard in 1983, 1988 and finally in 1999

It was eventually cracked and no longer considered secure solution. Consequently 3DES was developed.

3DES:
Triple DES is a Symmetric Key block cipher that uses a double DES block cipker - encrypt with the first key, delete encryption with the second key and encrypt again with the third key.

There is also a variation of the two keys where the first and second keys are duplicate of each other.

But 3DES was considered too slow for the growing need for fast communication channels and people eventually fell back to using DES.

RJINDAEL ALGORITHM:
Rjindael algorithm was introduced in 1998

AES:
It was replaced by AES in 2002
```

FEISTEL CIPHERS
------------------------------------------
```
- A feistel cipher is a block cipher that is used as a structure for encryption algorithms
- It uses substitutiion and permutation alternately
- It is based on Shannon Structure proposed in 1945
- Developed by Horst Feistel
- Reversing the process can decrypt ciphertext back to plaintext
```

HOW FEISTEL CIPHERS WORK
------------------------------------------
```
Encryption Process:
- The block being encrypted is divided into two parts.
- One part is passed onto the function, the other is XORed with the function's output. The function also uses the encryption key which differs for each individual 
- This goes on until the last step where the left hand side and right hand side are being swapped. here we receive our final cipher text

Decryption Process:
- The entire procedure is reversed starting from the order of the keys to the block sorting
- If the entire process is repeated in reverse order we eventually get back our plain text

This simplicity helps the speed but overall it was detrimental to efficiency of the algorithm, hence security was compromised
```


