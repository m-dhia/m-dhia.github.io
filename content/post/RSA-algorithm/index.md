---
title: RSA algorithm
description: "Exploring the RSA Algorithm: From Calculation to Implementation in Linux"
slug: rsa-algorithm
date: 2023-12-24 00:00:00+0000
categories:
    - Cybersecurity
tags:
    - Linux
---

# Understanding the RSA Algorithm

The RSA algorithm is a widely used  encryption algorithm that serve to secure data transmission over the internet. It is named after its inventors, Ron Rivest, Adi Shamir, and Leonard Adleman, who introduced it in 1977. This algorithm is based on the mathematical properties of large prime numbers and their factorization, which makes it computationally secure.

## How RSA Works

RSA is an asymmetric algorithm. It uses a pair of keys – a public key and a private key – to encrypt and decrypt data. The public key is shared with anons who wants to send encrypted data to the owner of the key, while the private key is kept secret and used by the key owner to decrypt the received data.

1. **Key Generation**:
   - Choose two distinct prime numbers, p and q.
   - Calculate n = p * q.
   - Calculate φ(n) = (p - 1) * (q - 1).
   - Choose an integer e such that 1 < e < φ(n) and gcd(e, φ(n)) = 1. This is the public exponent.
   - Calculate d = e^(-1) mod φ(n). This is the private exponent.

2. **Encryption**:
   - Convert the plaintext message into an integer m, where 0 < m < n.
   - Compute the ciphertext c = m^e mod n.

3. **Decryption**:
   - To decrypt the ciphertext c, compute the plaintext message m = c^d mod n.

## Example

Let's go through a simple example to illustrate how RSA works:

1. **Key Generation**:
   - Choose p = 61 and q = 53.
   - Calculate n = 61 * 53 = 3233.
   - Calculate φ(n) = (61 - 1) * (53 - 1) = 3120.
   - Choose e = 17.
   - Calculate d = 2753, since 17 * d ≡ 1 (mod 3120).

2. **Encryption**:
   - Assume we want to encrypt the message "HELLO".
   - Convert "HELLO" to its ASCII representation: H=72, E=69, L=76, L=76, O=79.
   - Combine the ASCII values: 7269767679.
   - Encrypt each block: 7269767679^17 mod 3233 = 2409 2754 1253 1253 1968.

3. **Decryption**:
   - To decrypt the ciphertext, we use the private key (d, n).
   - Decrypt each block: 2409^2753 mod 3233 = 72 (H), 2754^2753 mod 3233 = 69 (E), 1253^2753 mod 3233 = 76 (L), 1253^2753 mod 3233 = 76 (L), 1968^2753 mod 3233 = 79 (O).
   - Convert back to ASCII: 72=H, 69=E, 76=L, 76=L, 79=O.

## Using RSA in Linux

In Linux, you can use the `openssl` command-line tool to work with RSA encryption and decryption.

### Generating RSA Keys

To generate an RSA key pair, you can use the following command:

```bash
openssl genpkey -algorithm RSA -out private_key.pem -aes256
```

This command generates a new RSA private key and encrypts it with AES 256-bit encryption. You will be prompted to enter a passphrase to protect the private key.
You can then extract the public key from the private key using the following command:


```bash
openssl rsa -in private_key.pem -pubout -out public_key.pem
```

### Encrypting and Decrypting Data

Once you have generated your RSA key pair, you can use them to encrypt and decrypt data.

#### Encryption

To encrypt a file using the public key, you can use the following command:

```bash
openssl pkeyutl -encrypt -in plaintext.txt -out encrypted.txt -pubin -inkey public_key.pem
```
> - pubin: This option indicates that the input key specified with -inkey is a public key. This is necessary when using a public key for encryption.
> - inkey public_key.pem: This specifies the input file containing the public key (public_key.pem) that will be used for encryption.

This command encrypts the contents of plaintext.txt using the public key from public_key.pem and saves the encrypted data to encrypted.txt.

#### Decryption

To decrypt the encrypted file using the private key, you can use the following command:

```bash
openssl pkeyutl -decrypt -in encrypted.txt -out decrypted.txt -inkey private_key.pem
```
This command decrypts the contents of encrypted.txt using the private key from private_key.pem and saves the decrypted data to decrypted.txt.

