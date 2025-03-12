# CHA- Extremely simple encryption tools made with Rust. 


There have been numerous encryption apps that were touted as being a helper of PRIVACY- but in reality they were a form of malware. None of that crap nonsense here. CHA is a bunch of individual tools with one page codebases- extremely easy to audit or modify. They are all coded with Rust- which any reasonable person would trust over C or C++.  THIS REPO IS MAINTAINED, and input from the community is welcome. 


Some CHA applications use the XChaCha20-Poly1305 algorithm for encryption. In Chakey, the key is loaded from a file, while in Chapass the key is derived from a password using Argon2. However, the actual encryption/decryption process in both apps is handled by XChaCha20-Poly1305, ensuring authenticated encryption with a random 24-byte nonce.

Chaaes is an AES tool. I think Ai has to get WAY better in order to handle properly making AES apps. In contrast, XChaCha20-Poly1305 is MUCH SIMPLER to implemnent than AES. 

OTPAES is a One Time Pad app. 


