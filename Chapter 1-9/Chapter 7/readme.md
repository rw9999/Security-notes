# Cryptography and the Public Key Infrastructure

The practice of encoding information in a manner that it cannot be decoded without access to the required decryption key

Cryptography consists of two main operations: **encryption**, which transforms plain-text information into ciphertext using an encryption key, and **decryption**, which transforms ciphertext back into plain text using a decryption key.

A **cipher** is a method used to scramble or obfuscate characters to hide their value. Ciphering is the process of using a cipher to do that type of scrambling to a message.

The two primary types of nonmathematical cryptography, or ciphering methods, are **substitution** and **transposition**.

## 

### Substitution Ciphers

A type of coding or ciphering system that changes one character or symbol into another.

**Caesar cipher** - The system involves simply shifting all letters a certain number of spaces in the alphabet.

Decrypting a message encrypted with the Caesar cipher follows the reverse process.

ROT13, or “rotate 13,” is another simple substitution cipher. The ROT13 cipher works the same way as the Caesar cipher but rotates every letter 13 places in the alphabet.

##

### Polyalphabetic Substitution

One of the problems with substitution ciphers is that they did not change the underlying letter and word frequency of the text. One way to combat this was to have multiple substitution alphabets for the same message.

In a polyalphabetic substitution cipher, you might shift the first letter by three to the right, the second letter by two to the right, and the third letter by one to the left; then repeat this formula with the next three letters.

The most famous example of a polyalphabetic substitution from historical times was the **Vigenère cipher**.

It used a keyword to look up the cipher text in a table. 

The user would take the first letter in the text that they wanted to encrypt, go to the Vigenère table, and match that with the letter from the keyword in order to find the ciphertext letter. This would be repeated until the entire message was encrypted. Each letter in the keyword generated a different substitution alphabet. 

##

### Transposition Ciphers

A transposition cipher involves transposing or scrambling the letters in a certain manner.

Typically, a message is broken into blocks of equal size, and each block is then scrambled.

##

### Steganography

Steganography is the art of using cryptographic techniques to embed secret messages within another file.

Steganographic algorithms work by making alterations to the least significant bits of the many bits that make up image files. The changes are so minor that there is no appreciable effect on the viewed image.

This technique allows communicating parties to hide messages in plain sight—for example, they might embed a secret message within an illustration on an otherwise innocent web page.

Steganographers often embed their secret messages within images, video files, or audio files because these files are often so large that the secret message would easily be missed by even the most observant inspector.

Adding digital watermarks to documents to protect intellectual property is accomplished by means of steganography.

## Goals of Cryptography

Security practitioners use cryptographic systems to meet four fundamental goals: confidentiality, integrity, authentication, and nonrepudiation. Achieving each of these goals requires the satisfaction of a number of design requirements, and not all cryptosystems are intended to achieve all four goals.

### Confidentiality

Ensures that data remains private in three different situations: when it is at rest, when it is in transit, and when it is in use.

Confidentiality is perhaps the most widely cited goal of cryptosystems — the preservation of secrecy for stored information or for communications between individuals and groups.

Two main types of cryptosystems enforce confidentiality.

- **Symmetric cryptosystems** use a shared secret key available to all users of the cryptosystem.
  
- **Asymmetric cryptosystems** use individual combinations of public and private keys for each user of the system.

When developing a cryptographic system for the purpose of providing confidentiality, you must think about three types of data:

- Data at rest, or stored data, is that which resides in a permanent location awaiting access.
  
- Data in motion, or data on the wire, is data being transmitted across a network between two systems.

- Data in use is data that is stored in the active memory of a computer system where it may be accessed by a process running on that system.

**Obfuscation** is a concept closely related to confidentiality. It is the practice of making it intentionally difficult for humans to understand how code works. This technique is often used to hide the inner workings of software, particularly when it contains sensitive intellectual property.

##

### Integrity

Integrity ensures that data is not altered without authorization.

If integrity mechanisms are in place, the recipient of a message can be certain that the message received is identical to the message that was sent.

Similarly, integrity checks can ensure that stored data was not altered between the time it was created and the time it was accessed.

Integrity controls protect against all forms of alteration, including intentional alteration by a third party attempting to insert false information, intentional deletion of portions of the data, and unintentional alteration by faults in the transmission process.

Message integrity is enforced through the use of encrypted message digests, known as **digital signatures**, created upon transmission of a message.

The recipient of the message simply verifies that the message's digital signature is valid, ensuring that the message was not altered in transit. 

Integrity can be enforced by both public and secret key cryptosystems.

##

### Authentication

Authentication verifies the claimed identity of system users and is a major function of cryptosystems.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/b9ee3f37-0288-4c2a-a7a8-bf527ed7a9c8)

##

### Nonrepudiation

Nonrepudiation provides assurance to the recipient that the message was originated by the sender and not someone masquerading as the sender.

It also prevents the sender from claiming that they never sent the message in the first place (also known as **repudiating** the message).

Secret key, or symmetric key, cryptosystems (such as simple substitution ciphers) do not provide this guarantee of nonrepudiation.

Nonrepudiation is offered only by public key, or asymmetric, cryptosystems

## Cryptographic Concepts

Before a message is put into a coded form, it is known as a **plain-text** message and is represented by the letter P when encryption functions are described. 

The sender of a message uses a cryptographic algorithm to encrypt the plain-text message and produce a **ciphertext** message, represented by the letter C. 

This message is transmitted by some physical or electronic means to the recipient.

The recipient then uses a predetermined algorithm to decrypt the ciphertext message and retrieve the plaintext version

### Cryptographic Keys

All cryptographic algorithms rely on keys to maintain their security

For the most part, a key is nothing more than a number. It's usually a very large binary number, but it's a number nonetheless

Every algorithm has a specific key space. The key space is the range of values that are valid for use as a key for a specific algorithm

A key space is defined by its key length. Key length is nothing more than the number of binary bits (0s and 1s) in the key. The key space is the range between the key that has all 0s and the key that has all 1s. Or to state it another way, the key space is the range of numbers from 0 to 2 n, where n is the bit size of the key. So, a 128-bit key can have a value from 0 to 2128 (which is roughly 3.40282367 × 1038)

##

### The Kerchoff Principle

An **algorithm** is a set of rules, usually mathematical, that dictates how enciphering and deciphering processes are to take place

Most cryptographers follow the Kerchoff principle, a concept that makes algorithms known and public, allowing anyone to examine and test them

Specifically, the Kerchoff principle (also known as Kerchoff's assumption) is that a cryptographic system should be secure even if everything about the system, except the key, is public knowledge. The principle can be summed up as “The enemy knows the system.”

Cryptographic keys are sometimes referred to as **cryptovariables**

The art of creating and implementing secret codes and ciphers is known as **cryptography**.

This practice is paralleled by the art of **cryptanalysis**—the study of methods to defeat codes and ciphers. 

Together, cryptography and cryptanalysis are commonly referred to as **cryptology**.

Specific implementations of a code or cipher in hardware and software are known as **cryptosystems**

##

### Ciphers

Ciphers are the algorithms used to perform encryption and decryption operations

**Cipher suites** are the sets of ciphers and key lengths supported by a system. Modern ciphers fit into two major categories, describing their method of operation: 

- **Block ciphers** operate on “chunks,” or blocks, of a message and apply the encryption algorithm to an entire message block at the same time.

The transposition ciphers are examples of block ciphers. The simple algorithm used in the challenge-response algorithm takes an entire word and reverses its letters. The more complicated columnar transposition cipher works on an entire message (or a piece of a message) and encrypts it using the transposition algorithm and a secret keyword. Most modern encryption algorithms implement some type of block cipher. 


- **Stream ciphers** operate on one character or bit of a message (or data stream) at a time.

The one-time pad is also a stream cipher because the algorithm operates on each letter of the plaintext message independently. Stream ciphers can also function as a type of block cipher. In such operations, there is a buffer that fills up to real-time data that is then encrypted as a block and transmitted to the recipient.

## Modern Cryptography

Modern cryptosystems use computationally complex algorithms and long cryptographic keys to meet the cryptographic goals of confidentiality, integrity, authentication, and nonrepudiation.

### Cryptographic Secrecy

Modern cryptosystems do not rely on the secrecy of their algorithms. In fact, the algorithms for most cryptographic systems are widely available for public review in the accompanying literature and on the Internet. Opening algorithms to public scrutiny actually improves their security.

Widespread analysis of algorithms by the computer security community allows practitioners to discover and correct potential security vulnerabilities and ensure that the algorithms they use to protect their communications are as secure as possible.

Modern cryptosystems rely on the secrecy of one or more cryptographic keys used to personalize the algorithm for specific users or groups of users.

The length of a cryptographic key is an extremely important factor in determining the strength of the cryptosystem and the likelihood that the encryption will not be compromised through cryptanalytic techniques.

The rapid increase in computing power allows you to use increasingly long keys in your cryptographic efforts. However, this same computing power is also in the hands of cryptanalysts attempting to defeat the algorithms you use. Therefore, it's essential that you outpace adversaries by using sufficiently long keys that will defeat contemporary cryptanalysis efforts.

Additionally, if you want to improve the chance that your data will remain safe from cryptanalysis some time into the future, you must strive to use keys that will outpace the projected increase in cryptanalytic capability during the entire time period the data must be kept safe. For example, the advent of quantum computing may transform cryptography, rendering current cryptosystems insecure.

##

### Symmetric Key Algorithms

Symmetric key algorithms rely on a “shared secret” encryption key that is distributed to all members who participate in the communications.

This key is used by all parties to both encrypt and decrypt messages, so the sender and the receiver both possess a copy of the shared key.

The sender encrypts with the shared secret key and the receiver decrypts with it.

When large-sized keys are used, symmetric encryption is very difficult to break. It is primarily employed to perform bulk encryption and provides only for the security service of confidentiality.

Symmetric key cryptography can also be called secret key cryptography and private key cryptography.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/f3eca3f5-28e0-43aa-8485-c1ce58a41463)

Symmetric key cryptography has several weaknesses:

**Key distribution is a major problem.** - Parties must have a secure method of exchanging the secret key before establishing communications with a symmetric key protocol. If a secure electronic channel is not available, an offline key distribution method must often be used (that is, out-of-band exchange).

**Symmetric key cryptography does not implement nonrepudiation.** - Because any communicating party can encrypt and decrypt messages with the shared secret key, there is no way to prove where a given message originated.

**The algorithm is not scalable.** - It is extremely difficult for large groups to communicate using symmetric key cryptography. Secure private communication between individuals in the group could be achieved only if each possible combination of users shared a private key.

**Keys must be regenerated often.** - Each time a participant leaves the group, all keys known by that participant must be discarded.

The major strength of symmetric key cryptography is the great speed at which it can operate. Symmetric key encryption is very fast, often 1,000 to 10,000 times faster than asymmetric algorithms. By nature of the mathematics involved, symmetric key cryptography also naturally lends itself to hardware implementations, creating the opportunity for even higher-speed operations.

##

### Asymmetric Key Algorithms

Asymmetric key algorithms, also known as public key algorithms, provide a solution to the weaknesses of symmetric key encryption.

In these systems, each user has two keys: a public key, which is shared with all users, and a private key, which is kept secret and known only to the owner of the keypair.

Opposite and related keys must be used in tandem to encrypt and decrypt. In other words, if the public key encrypts a message, then only the corresponding private key can decrypt it, and vice versa.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/db866dd5-d2ba-4de9-b3f3-d3e2667bdbfb)

Asymmetric key algorithms also provide support for digital signature technology.

The following is a list of the major strengths of asymmetric key cryptography:

**The addition of new users requires the generation of only one public-private key pair.** -This same key pair is used to communicate with all users of the asymmetric cryptosystem. This makes the algorithm extremely scalable.

**Users can be removed far more easily from asymmetric systems.** - Asymmetric cryptosystems provide a key revocation mechanism that allows a key to be canceled, effectively removing a user from the system.

**Key regeneration is required only when a user's private key is compromised.** - If a user leaves the community, the system administrator simply needs to invalidate that user's keys. No other keys are compromised and therefore key regeneration is not required for any other user.

**Asymmetric key encryption can provide integrity, authentication, and nonrepudiation.** - If a user does not share their private key with other individuals, a message signed by that user can be shown to be accurate and from a specific source and cannot be later repudiated.

**Key distribution is a simple process** - Users who want to participate in the system simply make their public key available to anyone with whom they want to communicate. There is no method by which the private key can be derived from the public key.

**No preexisting communication link needs to exist.** - Two individuals can begin communicating securely from the start of their communication session. Asymmetric cryptography does not require a preexisting relationship to provide a secure mechanism for data exchange.

The major weakness of public key cryptography is its slow speed of operation. For this reason, many applications that require the secure transmission of large amounts of data use public key cryptography to establish a connection and then exchange a symmetric secret key. The remainder of the session then uses symmetric cryptography.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/3a5f9dd2-1df2-4eb7-a85a-9875d3be2217)

##

### Hashing Algorithms

Public key cryptosystems can provide digital signature capability when used in conjunction with a message digest.

Message digests are summaries of a message's content (not unlike a file checksum) produced by a hashing algorithm.

It's extremely difficult, if not impossible, to derive a message from an ideal hash function, and it's very unlikely that two messages will produce the same hash value.

Cases where a hash function produces the same value for two different methods are known as collisions, and the existence of **collisions** typically leads to the deprecation of a hashing algorithm.

##

### Key Requirements

The total number of keys required to completely connect n parties using symmetric cryptography is given by the following formula:

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/4d803ffc-e007-4577-913b-24d7eb97eb31)

The larger the population, the less likely a symmetric cryptosystem will be suitable to meet its needs.

![image](https://github.com/rw9999/Security-plus-notes/assets/134976895/2debd9b0-0212-4495-837e-e66477515a74)

##

### Data Encryption Standard

The U.S. government published the Data Encryption Standard in 1977 as a proposed standard cryptosystem for all government communications.

Because of flaws in the algorithm, cryptographers and the federal government no longer consider DES secure. It is widely believed that intelligence agencies routinely decrypt DESencrypted information.

DES was superseded by the Advanced Encryption Standard in December 2001

DES is a 64-bit block cipher that has five modes of operation: Electronic Codebook (ECB) mode, Cipher Block Chaining (CBC) mode, Cipher Feedback (CFB) mode, Output Feedback (OFB) mode, and Counter (CTR) mode.

All of the DES modes operate on 64 bits of plaintext at a time to generate 64-bit blocks of ciphertext. The key used by DES is 56 bits long.

DES uses a long series of exclusive or (XOR) operations to generate the ciphertext. This process is repeated 16 times for each encryption/decryption operation. Each repetition is commonly referred to as a round of encryption, explaining the statement that DES performs 16 rounds of encryption.

The DES specification calls for a 64- bit key. However, of those 64 bits, only 56 actually contain keying information. The remaining 8 bits are supposed to contain parity information to ensure that the other 56 bits are accurate. In practice, however, those parity bits are rarely used.

##

### Electronic Codebook Mode

Electronic Codebook (ECB) mode is the simplest mode to understand and the least secure.

Each time the algorithm processes a 64-bit block, it simply encrypts the block using the chosen secret key. This means that if the algorithm encounters the same block multiple times, it will produce the same encrypted block.

After a sufficient number of blocks were gathered, cryptanalytic techniques could be used to decipher some of the blocks and break the encryption scheme.

This vulnerability makes it impractical to use ECB mode on all but the shortest transmissions. In everyday use, ECB is used only for exchanging small amounts of data, such as keys and parameters used to initiate other DES modes as well as the cells in a database.

##

### Cipher Block Chaining Mode

In Cipher Block Chaining (CBC) mode, each block of unencrypted text is combined with the block of ciphertext immediately preceding it before it is encrypted using the DES algorithm. The decryption process simply decrypts the ciphertext and reverses the encryption operation.

CBC uses an **initialization vector** (IV), which is a randomly selected value that is used to start the encryption process. CBC takes the IV and combines it with the first block of the message using an operation known as the exclusive or (XOR), producing a unique output every time the operation is performed.

The IV must be sent to the recipient, perhaps by tacking the IV onto the front of the completed ciphertext in plain form or by protecting it with ECB mode encryption using the same key used for the message.

One important consideration when using CBC mode is that errors propagate—if one block is corrupted during transmission, it becomes impossible to decrypt that block and the next block as well.

##

### Cipher Feedback Mode

Cipher Feedback (CFB) mode is the streaming cipher version of CBC. In other words, CFB operates against data produced in real time.

However, instead of breaking a message into blocks, it uses memory buffers of the same block size. As the buffer becomes full, it is encrypted and then sent to the recipients. Then the system waits for the next buffer to be filled as the new data is generated before it is in turn encrypted and then transmitted.

Other than the change from preexisting data to real-time data, CFB operates in the same fashion as CBC.

##

### Output Feedback Mode

In Output Feedback (OFB) mode, DES operates in almost the same fashion as it does in CFB mode.

However, instead of XORing an encrypted version of the previous block of ciphertext, DES XORs the plain text with a seed value.

For the first encrypted block, an initialization vector is used to create the seed value. Future seed values are derived by running the DES algorithm on the previous seed value.

The major advantages of OFB mode are that there is no chaining function and transmission errors do not propagate to affect the decryption of future blocks.

##

### Counter Mode

DES that is run in Counter (CTR) mode uses a stream cipher similar to that used in CFB and OFB modes. However, instead of creating the seed value for each encryption/decryption operation from the results of the previous seed values, it uses a simple counter that increments for each operation. 

As with OFB mode, errors do not propagate in CTR mode.

CTR mode allows you to break an encryption or decryption operation into multiple independent steps. This makes CTR mode well suited for use in parallel computing.

##

### Triple DES

An adapted version of DES, Triple DES (3DES), uses the same algorithm to produce a more secure encryption.

There are four versions of 3DES. The first simply encrypts the plaintext three times, using three different keys: K<sub>1</sub>, K<sub>2</sub>, and K<sub>3</sub>.

It is known as DES-EEE3 mode (the Es indicate that there are three encryption operations, whereas the numeral 3 indicates that three different keys are used).

DES-EEE3 can be expressed using the following notation, where E(K,P) represents the encryption of plaintext P with key K:

    E(K1,E(K2,E(K3,P)))

DES-EEE3 has an effective key length of 168 bits.

The second variant (DES-EDE3) also uses three keys but replaces the second encryption operation with a decryption operation.

    E(K1,D(K2,E(K3,P)))

The third version of 3DES (DES-EEE2) uses only two keys, K1 and K2, as follows:

    E(K1,E(K2,E(K1,P)))

The fourth variant of 3DES (DES-EDE2) also uses two keys but uses a decryption operation in the middle, represented by the D(K,C) function, where K is the decryption key and C is the ciphertext to be decrypted.

    E(K1,D(K2,E(K1,P)))

Both the third and fourth variants have an effective key length of 112
bits.

These four variants of 3DES were developed over the years because several cryptologists put forth theories that one variant was more secure than the others. However, the current belief is that all modes are equally secure.

##

### Advanced Encryption Standard

In October 2000, the National Institute of Standards and Technology announced that the Rijndael block cipher had been chosen as the replacement for DES. In November 2001, NIST released FIPS 197, which mandated the use of AES/Rijndael for the encryption of all sensitive but unclassified data by the U.S. government.

The AES cipher allows the use of three key strengths: 128 bits, 192 bits, and 256 bits. AES only allows the processing of 128-bit blocks, but Rijndael exceeded this specification, allowing cryptographers to use a block size equal to the key length. The number of encryption rounds depends on the key length chosen:

- 128-bit keys require 10 rounds of encryption.
  
- 192-bit keys require 12 rounds of encryption.
  
- 256-bit keys require 14 rounds of encryption.

## Symmetric Key Management

It is incumbent upon cryptosystem users and administrators to take extraordinary measures to protect the security of the keying material. These security measures are collectively known as **key management practices**. They include safeguards surrounding the creation, distribution, storage, destruction, recovery, and escrow of secret keys.

## Creation and Distribution of Symmetric Keys

**Key exchange** is one of the major problems underlying symmetric encryption algorithms. Key exchange is the secure distribution of the secret keys required to operate the algorithms.

The three main methods used to exchange secret keys securely are offline distribution, public key encryption, and the Diffie–Hellman key exchange algorithm.

### Offline Distribution

The most technically simple method involves the physical exchange of key material.

One party provides the other party with a sheet of paper or piece of storage media containing the secret key.

In many hardware encryption devices, this key material comes in the form of an electronic device that resembles an actual key that is inserted into the encryption device.

However, every offline key distribution method has its own inherent flaws. If keying material is sent through the mail, it might be intercepted. Telephones can be wiretapped. Papers containing keys might be inadvertently thrown in the trash or lost.

##

### Public Key Encryption

Many communicators want to obtain the speed benefits of secret key encryption without the hassles of key distribution.

Many people use public key encryption to set up an initial communications link.

Once the link is successfully established and the parties are satisfied as to each other's identity, they exchange a secret key over the secure public key link. They then switch communications from the public key algorithm to the secret key algorithm and enjoy the increased processing speed.

In general, secret key encryption is thousands of times faster than public key encryption.

##

### Diffie–Hellman 

In some cases, neither public key encryption nor offline distribution is sufficient. Two parties might need to communicate with each other, but they have no physical means to exchange key material, and there is no public key infrastructure in place to facilitate the exchange of secret keys.

In situations like this, key exchange algorithms like the Diffie–Hellman algorithm prove to be extremely useful mechanisms.

The algorithm works as follows:

1. The communicating parties (we'll call them Richard and Sue) agree on two large numbers: p (which is a prime number) and g (which is an integer) such that 1 < g < p.

2. Richard chooses a random large integer r and performs the following calculation:

        R = gr mod p
   
3. Sue chooses a random large integer s and performs the following calculation:

        S = gs mod p

4. Richard sends R to Sue and Sue sends S to Richard.     

5. Richard then performs the following calculation:

        K = Sr mod p

6. Sue then performs the following calculation:

       K = Rs mod p

At this point, Richard and Sue both have the same value, K, and can use this for secret key communication between the two parties.

##

### Storage and Destruction of Symmetric Keys

Another major challenge with the use of symmetric key cryptography is that all of the keys used in the cryptosystem must be kept secure.

This includes the following best practices surrounding the storage of encryption keys:

- Never store an encryption key on the same system where encrypted data resides.
  
- For sensitive keys, consider providing two different individuals with half of the key. They then must collaborate to re-create the entire key. This is known as the principle of **split knowledge**

When a user with knowledge of a secret key leaves the organization or is no longer permitted access to material protected with that key, the keys must be changed, and all encrypted materials must be reencrypted with the new keys. 

The difficulty of destroying a key to remove a user from a symmetric cryptosystem is one of the main reasons organizations turn to asymmetric algorithms.

##

### Key Escrow and Recovery

To gain a handle on the explosive growth of cryptographic technologies, governments around the world have floated ideas to implement key escrow systems.

These systems allow the government, under limited circumstances such as a court order, to obtain the cryptographic key used for a particular communication from a central storage facility.

There are two major approaches to key escrow:

**Fair Cryptosystems** - In this escrow approach, the secret keys used in a communication are divided into two or more pieces, each of which is given to an independent third party.

Each of these pieces is useless on its own but may be recombined to obtain the secret key. When the government obtains legal authority to access a particular key, it provides evidence of the court order to each of the third parties and then reassembles the secret key.

**Escrowed Encryption Standard** - This escrow approach provides the government with a technological means to decrypt ciphertext. This standard is the basis behind the Skipjack algorithm.

It's highly unlikely that government regulators will ever overcome the legal and privacy hurdles necessary to implement key escrow on a widespread basis.

The technology is certainly available, but the general public will likely never accept the potential government intrusiveness it facilitates.

## Asymmetric Cryptography

Public key cryptosystems rely on pairs of keys assigned to each user of the cryptosystem. Every user maintains both a public key and a private key. As the names imply, public key cryptosystem users make their public keys freely available to anyone with whom they want to communicate.

The mere possession of the public key by third parties does not introduce any weaknesses into the cryptosystem. The private key, on the other hand, is reserved for the sole use of the individual who owns the keys. It is never shared with any other cryptosystem user.

Keys used within public key systems must be longer than those used in private key systems to produce cryptosystems of equivalent strengths

### RSA

In 1977, Ronald Rivest, Adi Shamir, and Leonard Adleman proposed the RSA public key algorithm that remains a worldwide standard today.

They patented their algorithm and formed a commercial venture known as RSA Security to develop mainstream implementations of their security technology.

The RSA algorithm has been released into the public domain and is widely used for secure communication.

The RSA algorithm depends on the computational difficulty inherent in factoring large prime numbers. Each user of the cryptosystem generates a pair of public and private keys using the algorithm.

##

### Importance of Key Length

The length of the cryptographic key is perhaps the most important security parameter that can be set at the discretion of the security administrator.

It's important to understand the capabilities of your encryption algorithm and choose a key length that provides an appropriate level of protection. This judgment can be made by weighing the difficulty of defeating a given key length (measured in the amount of processing time required to defeat the cryptosystem) against the importance of the data.

The more critical your data, the stronger the key you use to protect it should be.

Timeliness of the data is also an important consideration. You must take into account the rapid growth of computing power—Moore's law suggests that computing power doubles approximately every two years.

Attackers are now able to leverage cloud computing resources, they are able to more efficiently attack encrypted data. The cloud allows attackers to rent scalable computing power, including powerful graphic processing units (GPUs) on a per hour basis and offers significant discounts when using excess capacity during non-peak hours. This brings powerful computing well within reach of many attackers.

The strengths of various key lengths also vary greatly according to the cryptosystem you're using.

Longer keys are certainly more secure, but they also require more computational overhead. It's the classic trade-off of resources versus security constraints.

##

### Elliptic Curve

In 1985, two mathematicians, Neal Koblitz from the University of Washington and Victor Miller from IBM, independently proposed the application of **elliptic curve cryptography** (ECC) theory to develop secure cryptographic systems.

Any elliptic curve can be defined by the following equation:

y<sup>2</sup> = x<sup>3</sup> + ax + b

In this equation, x, y, a, and b are all real numbers. Each elliptic curve has a corresponding **elliptic curve group** made up of the points on the elliptic curve along with the point O, located at infinity. Two points within the same elliptic curve group (P and Q) can be added together with an elliptic curve addition algorithm. This operation is expressed as

P + Q

This problem can be extended to involve multiplication by assuming that Q is a multiple of P, meaning the following:

Q = xP

Computer scientists and mathematicians believe that it is extremely hard to find x, even if P and Q are already known. This difficult problem, known as the elliptic curve discrete logarithm problem, forms the basis of elliptic curve cryptography. It is widely believed that this problem is harder to solve than both the prime factorization problem that the RSA cryptosystem is based on and the standard discrete logarithm problem utilized by Diffie–Hellman.

## Hash Functions

Hash functions have a very simple purpose—they take a potentially long message and generate a unique output value derived from the content of the message.

This value is commonly referred to as the **message digest**. Message digests can be generated by the sender of a message and transmitted to the recipient along with the full message for two reasons.

First, the recipient can use the same hash function to recompute the message digest from the full message. They can then compare the computed message digest to the transmitted one to ensure that the message sent by the originator is the same one received by the recipient. If the message digests do not match, that means the message was somehow modified while in transit.

It is important to note that the messages must be exactly identical for the digests to match. If the messages have even a slight difference in spacing, punctuation, or content, the message digest values will be completely different.

It is not possible to tell the degree of difference between two messages by comparing the digests. Even a slight difference will generate totally different digest values.

The term message digest is used interchangeably with a wide variety of synonyms, including hash, hash value, hash total, CRC, fingerprint, checksum, and digital ID.

There are five basic requirements for a cryptographic hash function:

- They accept an input of any length.
  
- They produce an output of a fixed length, regardless of the length of the input.
  
- The hash value is relatively easy to compute.
  
- The hash function is one-way (meaning that it is extremely hard to determine the input when provided with the output).
  
- The hash function is collision free (meaning that it is extremely hard to find two messages that produce the same hash value).

##

### SHA

