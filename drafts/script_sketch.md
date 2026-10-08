# Very rough draft of the actual script 
<!-- Currently just a template --->
## Intro



## Topic 1. RSA key generation

So to start off, first we need to take two very large random prime numbers, in UNIX systems this can be achieved by converting the infinitely generating output of /dev/urandom into hexidecimal, how big of a number you want is directly tied to how many bits are recieved from urandom. The typical length is 2048 bits. 

### Private key

Since RSA works by encrypting and decryping via a linked private & public key, we will generate it using *"Euler's Totient Function"* ***(TAKE OUT THIS IF NEEDED)-->*** the function is phi n, first prime minus 1 multiplied by the second prime minus 1 ***<---*** Then a public exponent *e* is selected, generally this exponent is 65537, and coprime with phi n. Now we can make a public key using e and n *(e,n)*

### Public key

Lastly we can generate our private exponent, *"d"*, which is the modular inverse of e. Thus the private key is d and n *(d,n)*

## Topic 2. How it's most commonly used (SSH)

Asymmetric encryption algorithims, *like RSA*, can be used anytime a client wants to send out and recieve data securely, if you're ever worried about being on a public network and fear that a bad actor could intercept your data and use that to send malicious data to your connectee (which is why http over public networks is a horrible idea), you don't have to be, as RSA uses a keypair and you cannot derive the private key from the public key, so even if you do this entire setup process over a open network it's still secure.

A few more specific use cases are openssh's ssh program, which connect you to a virtual terminal on whatever server you choose to connect to as the user you decided to connect as. General end-to-end encryption on any platform, such as whatsapp, imessage, and mostly importantly HTTPS, which is the bases of the entire modern internet.


## Closeoff, wrap it up






<!-- Doesn't seem like that much when you(me) put it like this! --->
<!-- Seriously, it seems to little, did i forget to add something? -->
