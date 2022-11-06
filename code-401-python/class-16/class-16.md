# Encryption, decryption, and cracking

## One of the earliest encryption techniques is the Caesar Cipher

**The Caesar Cipher is a simple substitution cipher which replaces each original letter with a different letter in the alphabet by shifting the alphabet by a certain amount.**

### Decrypting a message

**According to historical records, Caesar always used a shift of 3. As long as his message recipient knew the shift amount, it was trivial for them to decode the message.**

### Cracking the cipher

**crack" the cipher without knowing the shift.**

### There are three main techniques he could use: frequency analysis, known plaintext, and brute force.

### Frequency analysis

**Human languages tend to use some letters more than others. For example, "E" is the most popular letter in the English language. We can analyze the frequency of the characters in the message and identify the most likely "E" and narrow down the possible shift amounts based on that.**

### Known plaintext

**Another term for the original unencrypted message is plaintext. If the enemy already knew some part of the plaintext, it will be easier for them to crack the rest of the encrypted version.**


### Brute force

**There are only 25 possible shifts (not 26 — why not?). The enemy could take some time to try out each of them and find one that yielded a sensible message. They wouldn't even need to try the shifts on the entire message, just the first word or two.**


- Encryption: scrambling the data according to a secret key (in this case, the alphabet shift).

- Decryption: recovering the original data from scrambled data by using the secret key.

- Code cracking: uncovering the original data without knowing the secret, by using a variety of clever techniques.

### Caesar cipher :

**is one of the simplest and most widely known encryption techniques. It is a type of substitution cipher in which each letter in the plaintext is replaced by a letter some fixed number of positions down the alphabet.**

A = D
B = E
C = F
D = G
E = H
F = I
And so on.

### The Caesar cipher can be easily broken even in a ciphertext-only scenario. Two situations can be considered:

- **an attacker knows (or guesses) that some sort of simple substitution cipher has been used, but not specifically that it is a Caesar scheme;**

- **an attacker knows that a Caesar cipher is in use, but does not know the shift value.**

###  Types of Cryptography

1. - Hashing

Hashing is a type of cryptography that changes a message into an unreadable string of text for the purpose of verifying the message’s contents, not hiding the message itself.

2. - Symmetric Cryptography

Symmetric Cryptography, likely the most traditional form of cryptography, is also the system with which you are probably most familiar.  

This type of cryptography uses a single key to encrypt a message and then decrypt that message upon delivery.

3.-  Asymmetric Cryptography
Asymmetric cryptography (as the name suggests) uses two different keys for encryption and decryption, as opposed to the single key used in symmetric cryptography.

4.-  Key Exchange Algorithms
Although this particular type of cryptography isn’t particularly applicable for individuals outside of the cyber-security realm, I wanted to briefly mention to ensure you have a full understanding of the different cryptographic algorithms.

