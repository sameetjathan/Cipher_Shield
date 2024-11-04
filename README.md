# Cipher Shield - File Encryption and Decryption Tool

Cipher Shield is a secure file encryption and decryption tool developed in Java and HTML/CSS, ensuring authorized access to sensitive data. With the AES-GCM encryption algorithm, Cipher Shield is designed to secure various file types and offers advanced functionality through both server and client hardware.

---

## 1. Server Infrastructure and Security

### Server Hardware
- **Processor**: Intel i5
- **Memory**: 8 - 16 GB RAM
- **Storage**: 512 GB SSD
- **Network Speed**: 10 MB/s

### Security Hardware
- **Hardware Security Modules (HSMs)**: Ensures secure cryptographic processing and key management.

### Additional Features
- **Load Balancing**: Distributes traffic to maintain high availability.
- **Scalability**: Designed for future hardware upgrades and mobile compatibility.

---

## 2. Software Details

### Frontend
- **Languages**: HTML and CSS for a seamless, user-friendly interface.

### Backend
- **Languages**: Java and JavaScript with AES-GCM encryption.
- **Encryption Algorithm**: 
  - **AES-GCM (Advanced Encryption Standard in Galois/Counter Mode)**: Provides both confidentiality and data integrity.
  - **Encryption Process**: Operates on 128, 192, or 256-bit keys and includes multiple rounds of cryptographic transformations.
  
### Key Encryption/Decryption Process
- **Key Generation**: 128-bit encryption keys are generated using Web Crypto API.
- **Encryption**: AES-GCM mode encrypts files with an authentication tag to ensure data integrity.
- **Decryption**: Utilizes the same AES-GCM algorithm for secure file decryption with authentication tag verification.

---

## 3. AES-GCM Encryption and Decryption Processes

### AES-GCM Encryption Steps
1. **Input**: Plaintext, encryption key, and Initialization Vector (IV).
2. **Rounds**: Initial XOR with round key, followed by multiple encryption rounds including SubBytes, ShiftRows, MixColumns, and AddRoundKey.
3. **Authentication Tag Generation**: Creates a Message Authentication Code (MAC) for integrity.
4. **Output**: Encrypted data (ciphertext) with an authentication tag.

### AES-GCM Decryption Steps
1. **Input**: Ciphertext, decryption key, IV, and authentication tag.
2. **Rounds**: Initial XOR and reverse operations (Inverse ShiftRows, Inverse SubBytes).
3. **Authentication Tag Verification**: Confirms data integrity.
4. **Output**: Decrypted data if authentication is successful.
