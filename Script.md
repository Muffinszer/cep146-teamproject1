# CEP146 — RSA Encryption Video Script

---

## Slide 1 — RSA Encryption

This presentation will focus on how RSA encryption works, how its keys are generated, and how it is used in the real world.

## Slide 2 — How RSA Encryption Works

RSA is an asymmetric encryption algorithm that uses a pair of mathematically linked keys: a public key and a private key.

The public key can be shared openly, while the private key must remain secret.

To send an encrypted message, the sender uses the recipient's public key. Only the corresponding private key can decrypt it.

For two-way communication, both parties can use their own key pairs to exchange encrypted information.

## Slide 3 — How They're Used and Made

Now that we understand the basic concept of RSA encryption, let's take a closer look at how public and private keys are generated and how they work together to provide secure communication.

## Slide 4 — RSA Key Generation

To generate RSA keys, we select two very large, random prime numbers and multiply them together to get a number called *n*. 

Next, we calculate Euler's totient function, or phi of n, by subtracting one from each prime number and multiplying the results. We then choose a public exponent, *e*, that is coprime with phi of n. Together, *e* and *n* form our public key. 

Finally, we calculate the private exponent, *d*, by finding the modular inverse of *e*. This gives us our private key, consisting of *d* and *n*.

## Slide 5 — Practicality in the Real World

In practice, encryption alone cannot guarantee that a public key belongs to the intended recipient.

An attacker could replace that key with their own and intercept communications. This is known as a Man-in-the-Middle attack.

To prevent these attacks, websites use digital certificates signed by trusted Authorities, which allow clients to verify that the public key belongs to the intended server.

## Slide 6 — Real World Usage

RSA is commonly used for authentication and digital signatures in secure communication systems.

For example, SSH allows users to securely connect to remote servers and can use RSA keys for authentication.

HTTPS also uses certificates and cryptographic algorithms to authenticate websites and establish secure connections, protecting information transmitted over public networks

## Slide 7 — The Future

RSA remains widely used today, but quantum computing presents a potential future threat.

Powerful quantum computers could eventually break RSA by efficiently factoring large numbers.

As a result, the National Institute of Standards and Technology is guiding a transition toward post-quantum cryptography, with major milestones in 2030 and 2035.

## Slide 8 — Closing Off

In conclusion, RSA demonstrates how public-key cryptography helps protect digital communications.

Without secure cryptographic systems, sensitive information would be much more vulnerable to interception.

Thank you for listening to our presentation.

## Slide 9 — Bibliography
No narration required.
