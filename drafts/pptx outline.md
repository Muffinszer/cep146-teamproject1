# Presentation's Outline

## Introduction

**Slide 1:**
- Title: RSA Encryption
- Subtitle: How RSA Works, Real-World Applications, and Future Challenges
- Content:
  1. Group members' names and student IDs
  2. Course: CEP146 NBB

## How Does RSA Encryption Work?

**Slide 2:**
- Title: How RSA Encryption Works
- Content:
  1. RSA is an asymmetric encryption algorithm.
  2. It uses two mathematically linked keys:
     1. Public Key: Can be shared openly.
     2. Private Key: Must remain secret.
  3. The sender encrypts data using the recipient's public key.
  4. The recipient decrypts data using their private key.
  5. Both parties can use their own key pairs for two-way communication.
- Visual: Encryption diagram illustrating public and private keys.

**Slide 3:**
- Title: How They're Used and Made
- Content:
  1. Introduce how public and private keys are generated.
  2. Transition to the mathematical process of RSA key generation.
- Visual: RSA encryption and decryption diagram.

## Topic 1. RSA Key Generation

**Slide 4:**
- Title: RSA Key Generation
- Subtitle: Public and Private Keys
- Content:
  1. Step 1: Select Prime Numbers
     1. Generate two large random prime numbers: p and q.
     2. Calculate n = p × q.
     3. RSA keys are commonly 2048 bits.
  2. Step 2: Generate the Public Key
     1. Calculate Euler's totient: φ(n) = (p − 1)(q − 1).
     2. Select a public exponent e, usually 65537.
     3. Ensure e is coprime with φ(n).
     4. Public key: (e, n).
  3. Step 3: Generate the Private Key
     1. Calculate d as the modular inverse of e modulo φ(n).
     2. Private key: (d, n).
- Visual: AI-generated RSA key-generation infographic.

## Topic 2. Practicality in the Real World

**Slide 5:**
- Title: Practicality in the Real World
- Subtitle: Digital Certificates
- Content:
  1. Encryption alone cannot verify a server's identity.
  2. Attackers can attempt Man-in-the-Middle (MITM) attacks by substituting public keys.
  3. Digital certificates are signed by trusted Certificate Authorities (CAs).
  4. Certificates bind public keys to verified identities.
  5. Proper certificate validation helps prevent MITM attacks.
- Visual: Man-in-the-Middle attack diagram.

## Topic 3. Real-World Applications

**Slide 6:**
- Title: Practicality in the Real World
- Subtitle: SSH and HTTPS
- Content:
  1. SSH (Secure Shell)
     1. Connects users securely to remote servers.
     2. Can use RSA key pairs for authentication.
  2. HTTPS (Hypertext Transfer Protocol Secure)
     1. Uses TLS to establish secure connections.
     2. Uses digital certificates for server authentication.
     3. RSA can be used for digital signatures.
     4. Modern HTTPS encrypts transmitted data using symmetric encryption.
  3. Security Benefits
     1. Protects against unauthorized access and impersonation.
     2. Public keys can be shared without revealing private keys.
- Visual: SSH and HTTPS illustration.

## Topic 4. The Future of RSA Encryption

**Slide 7:**
- Title: The Future of RSA Encryption
- Content:
  1. RSA remains widely used today.
  2. Quantum computing presents a potential future security threat.
  3. Sufficiently powerful quantum computers could break RSA encryption.
  4. NIST is guiding the transition to post-quantum cryptography.
  5. Major proposed transition milestones: 2030 and 2035.
- Visual: Encryption timeline illustrating the development of cryptographic algorithms.

## Conclusion

**Slide 8:**
- Title: Closing Off
- Content:
  1. Summarize how RSA uses asymmetric cryptography.
  2. Emphasize the importance of public and private keys in securing communications.
  3. Highlight RSA's real-world applications.
  4. Acknowledge future challenges from quantum computing.
  5. Thank the audience.
- Visual: Public-key and private-key encryption diagram.

## Bibliography

**Slide 9:**
- Title: Bibliography
- Content:
  1. Academic and technical references.
  2. Sources related to RSA encryption, key generation, and quantum computing.
  3. Figure references and image attributions.

**Slide 10:**
- Title: Bibliography
- Content:
  1. Remaining academic and technical references.
  2. Sources related to TLS, SSH, and digital certificates.
  3. Additional figure references.
