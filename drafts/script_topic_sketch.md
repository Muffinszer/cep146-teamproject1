# THIS IS NOT THE SCRIPT
===========================

Declaring the basics of RSA encryption:

1. Select two *Very* large prime numbers. in linux there is a non-existent device called "urandom" (full path /dev/urandom), note that there is a /dev/random, the problem is that when the kernal declares that there has been an *inadequate* amount of entropy (generated from raw external input, I.E. Mouse input, tempature readings, Electricty draw, and much, MUCH more.) Since this isn't a talk about how that works i'll leave it there.

2. Generate public and private keys. Easier said than done. using the 2 primes from before, we will put them into a function called "Euler's totient function", it looks like this: **φ(n) = (p – 1)(q – 1)** then a public exponent *e* is selected which is usually 65537, that is coprime with φ(n). The public key is the pair (e,n).

- Now, we have the private exponent *d*, which is the modular inverse of *e*. Meaning **e x d = 1(mod φ(n))**. The private key is (d, n)

### And that's it. (for just setting up the key)


## This part is for encrypting messages and decrypting them, specifically ssh

- Before i get into anything, just know that as the client, (the one connecting to the server), you ONLY are providing your public key to the server, NOT your private key. And to be clear the server also has a key pair just like a client does, you download the server's public key when you type (yes) when connecting to a server for the first time (the server doesn't generate one on every new client, the server *generally* just has a single keypair shared with all of its clients.)

### Encrypting

- The sender has a command in plain text "echo hi", and converts those characters into a number of some sort (multiple options), then we generate the encrypted text *c* using their public *e* **c = m^e mod n**.  

### Decrypting

- The recipient uses their private key to decrypt the recieved message: **m = c^d mod n**. we just use the linked private key as that'll result in the same answer.




# Example c code

<!--- TODO: I have done most of the program but generating keys in c require an annoying library to work with (GMP library), i may just throw away and start again but using default var types, not viable for actual use case but it's example code so who cares.--->
