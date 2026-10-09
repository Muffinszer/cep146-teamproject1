# Very rough draft of actual script

## Intro

This presentation will focus on how RSA works, how they're made, and how they
are used!

## How does RSA encryption even work?

RSA encryption is a type of asymmetric encryption algorithim, generating a key
pair to encrypt and decrypt data. For this presentation we will be focusing on
two way communication as that is it's most common form. How we achieve this is
after we make the key pair, we send our recipient the public (in plaintext) key
while we keep the private key, then the recipient uses the public key to encrypt
and send over their own public key, note that it is encrypted while ours isn't
since we need to know it was the server who sent us the proper key, as we use
our own private key to decrypt their public key. Thus two way secure information
is provided, allowing both to send and recieve data, encrypting through the
other's public key and decrypting with your own private key.

## Topic 1. RSA key generation

So to start off, first we need to take two very large random prime numbers, in
UNIX systems this can be achieved by converting the infinitely generating output
of /dev/urandom into hexidecimal, how big of a number you want is directly tied
to how many bits are recieved from urandom. The typical length is 2048 bits.

### Private key

Since RSA works by encrypting and decryping via a linked private & public key,
we will generate it using "Euler's Totient Function" (TAKE OUT THIS IF
NEEDED)--> the function is phi n, first prime minus 1 multiplied by the second
prime minus 1 <--- Then a public exponent e is selected, generally this exponent
is 65537, and coprime with phi n. Now we can make a public key using e and n
(e,n)

### Public key

Lastly we can generate our private exponent, "d", which is the modular inverse
of e. Thus the private key is d and n (d,n)

## Topic 2. How it's most commonly used (SSH)

Asymmetric encryption algorithims, like RSA, can be used anytime a client wants
to send out and recieve data securely, if you're ever worried about being on a
public network and fear that a bad actor could intercept your data and use that
to send malicious data to your connectee (which is why http over public networks
is a horrible idea), you don't have to be, as RSA uses a keypair and you cannot
derive the private key from the public key, so even if you do this entire setup
process over a open network it's still secure.

A few more specific use cases are openssh's ssh program, which connect you to a
virtual terminal on whatever server you choose to connect to as the user you
decided to connect as. General end-to-end encryption on any platform, such as
whatsapp, imessage, and mostly importantly HTTPS, which is the bases of the
entire modern internet.

## Closeoff, wrap it up

This was a quick runthrough on how encryption algorithims work and their
usefulness to the world, as without them we'd have any and all information
easily interceptable whether at the cafe, at your job, or even your own ISP.
Thank you for your time.

<!-- Doesn't seem like that much when you(me) put it like this! --->

<!-- Seriously, it seems to little, did i forget to add something? -->

