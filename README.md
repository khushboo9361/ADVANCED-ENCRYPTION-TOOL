# AES Encryption with PyCrypto

**Company**: CODETECH IT SOLUTIONS  

**Name**  : KHUSHBOO KUMARI

**Id**: CT08HQE

**Domain**: CYBER SECURITY AND ETHICAL HACKING  

**Batch Duration**: Dec 30th 2024 to Jan 30th, 2025 

*Mentor Name**: NEELA SANTHOSH
---




This project demonstrates the implementation of AES encryption using the `pycrypto` library in Python. The core components of this project involve cryptographic techniques, including key generation, encryption, and decryption processes, aimed at securing data through strong encryption mechanisms.

## Overview

This project provides a Python implementation of AES (Advanced Encryption Standard) encryption using the `pycrypto` library. The key aspects of the project include:
- **AES Encryption**: The main focus of the project is to demonstrate AES encryption with a 256-bit key and 128-bit IV (Initialization Vector).
- **Key Management**: The project showcases how to generate secure keys and IVs.
- **Salt Generation**: A random salt is used to enhance the security of the encryption process.
- **AES Mode**: It uses the AES algorithm in CBC (Cipher Block Chaining) mode for encryption.
  
## Features

- **Key Generation**: Utilizes a 256-bit AES key with a 128-bit IV for encryption.
- **Encryption/Decryption**: Supports both the encryption and decryption of files or messages.
- **Salt Handling**: Secure random salt is used to strengthen the encryption.
- **File Security**: The encryption process can be applied to both small data and files.
  
## Requirements

- Python 3.x
- pycrypto library: `pip install pycrypto`
- hashlib (for creating hash-based keys)
- os (for handling random operations)

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/pycrypto-aes-encryption.git
cd pycrypto-aes-encryption
```

Install dependencies:

```bash
pip install pycrypto
```

## Usage

Once the dependencies are installed, you can use the provided methods to encrypt and decrypt messages or files.

### Encrypting Data

To encrypt data, run the following script:

```python
from Crypto.Cipher import AES
import os
import hashlib

# AES Encryption parameters
IV_SIZE = 16
KEY_SIZE = 32
SALT_SIZE = 16

def encrypt(data, key):
    cipher = AES.new(key, AES.MODE_CBC, iv=os.urandom(IV_SIZE))
    return cipher.encrypt(data)

# Example usage
key = os.urandom(KEY_SIZE)  # Generate a random key
data = b"Your data to encrypt"
encrypted_data = encrypt(data, key)
```

### Decrypting Data

To decrypt the encrypted data:

```python
def decrypt(encrypted_data, key):
    cipher = AES.new(key, AES.MODE_CBC, iv=os.urandom(IV_SIZE))
    return cipher.decrypt(encrypted_data)

# Example usage
decrypted_data = decrypt(encrypted_data, key)
```

## Project Structure

- `README.md`: This file.
- `encryption.py`: Main encryption/decryption logic.
- `utils.py`: Utility functions for key generation, salt, etc.
- `example.py`: Example usage of encryption and decryption.

## Contributions

Feel free to fork this repository and create pull requests. Contributions are welcome!

--- 
