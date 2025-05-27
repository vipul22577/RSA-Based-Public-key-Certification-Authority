# RSA-based-Public-key-Certification-Authority-CA-
Overview
This project implements a simplified RSA-based Public-Key Certification Authority (CA) system along with two clients that securely request and exchange public key certificates. The system enables clients to communicate confidentially by encrypting messages with the receiver’s verified public key.

Features
RSA Key Generation:
Each client generates its own RSA key pair (private and public keys) using large 1024-bit prime numbers and standard RSA algorithms.

Certification Authority (CA):
The CA issues digitally signed public-key certificates to clients upon request. Certificates include client ID, public key, issuance time, validity duration, and CA identity.

Certificate Format:
Certificates consist of the original data concatenated with a SHA-256 encrypted digital signature created with the CA’s private key.

Certificate Registration and Verification:
Clients register with the CA by submitting their ID and public key. The CA stores this information and issues signed certificates. Clients verify certificates using the CA’s public key to ensure authenticity and prevent tampering.

Secure Public Key Distribution:
Clients obtain others’ public keys securely via the CA, preventing spoofing and ensuring trusted communication.

Encrypted Messaging:
Clients exchange messages encrypted with the receiver’s public key and decrypted with the receiver’s private key. The example exchange includes sending “Hello1”, “Hello2”, “Hello3” and receiving corresponding acknowledgments.
