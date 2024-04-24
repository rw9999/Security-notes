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





