# Presentation's outline

## Introduction

**Slide 1:** 
- Title: RSA Encryption
- Subtitle: How they're made, and how they are used!

## How does RSA encryption theoretically works?
> Maybe combine both slides into 1 ????
> TO DO: Add some pictures

**Slide 2:** 
- Title: How RSA works?
- Sub title: Fundamentals
- Content:
  1. RSA is an asymmetric encryption algorithm
  2. It creates two keys:
     1. Public Key: Can be shared
     2. Private Key: Kept secret
  3. Encrypted data with public key can be decrypted only with the matching private key
 
**Slide 3:**
- Title: How RSA works?
- Sub title: Communication
- Content:
  1. Both sides generate their own key pair
  2. Exchange public keys
  3. Data encrypted using other's public key
  4. Data decrypted using own private key

## Topic 1. RSA key generation

**Slide 4:**
- Title: RSA Key Generation
- Content:
  1. Generate two large prime numbers p & q
  2. Generate public key
     1. Public exponent e, commonly 65537
     2. e must coprime with phi n
     3. Public key = (e, n)
  3. Generate private key
     1. Calculate d as the modular inverse of e
     2. Private key = (d, n)
- Images:
  1. Calculations, to find

## Topic 2. How does it practically work in the real world?

**Slide 5:**
- Title: How RSA works in the world
- Sub title: Man in the Middle Attack
- Content:
  1. Problem - Attacker substitutes public key
  2. Solutions - Certificates binds Public Key to Domain
  3. Verification: Trusted CA signs certificate, client verifies signature
 - Image:
   1. MITM attack img

## Topic 3. How it's most commonly used (SSH)

**Slide 6.**
- Title: How RSA works in the world
- Sub title: Real world usage
- Content:
  1. Safe in public networks
  2. SSH:
     1. Secure remote terminal access
     2. Public end to end key cryptography
     3. Asymmetric keys are used for the connection
  3. HTTPS
     1. Authenticates websites using certificates
     2. Established a secure session
- Image:
  1. To do
 
