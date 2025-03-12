# CHA- secure encryption tools


Ai can make you 10 or more encryption apps every single minute. CHA is a more focused approach. 


CHA applications use the XChaCha20-Poly1305 algorithm for encryption. In Chakey, the key is loaded from a file, while in Chapass the key is derived from a password using Argon2. However, the actual encryption/decryption process in both apps is handled by XChaCha20-Poly1305, ensuring authenticated encryption with a random 24-byte nonce.

XChaCha20-Poly1305 is an authenticated encryption with associated data (AEAD) construction that combines the XChaCha20 stream cipher with the Poly1305 message authenticator. It is designed to provide both confidentiality and integrity, ensuring that encrypted data remains secret and tamper-evident. Like AES, it is intended to secure sensitive information; however, it achieves this with a different approach that emphasizes simplicity and robustness in software implementations.

One of the key advantages of XChaCha20-Poly1305 is its ease of use compared to many AES modes. While AES is a well-established standard and widely trusted, it often requires careful implementation of modes like GCM or CBC to avoid vulnerabilities such as nonce reuse and side-channel attacks. In contrast, XChaCha20-Poly1305 simplifies many of these challenges by using an extended 192-bit nonce, which significantly reduces the risk of nonce collisions even in scenarios where nonce management might be less rigorous. This makes it an excellent choice for single users or small projects where implementing a secure AES setup might be too complex.

Additionally, XChaCha20-Poly1305 does not rely on any special hardware features, unlike AES which can benefit from dedicated hardware instructions found in modern processors. This means that XChaCha20-Poly1305 is not only highly portable across different platforms, but it also performs well in pure software environments. Its design is optimized for ease of implementation, lowering the barrier for developers to securely encrypt data without needing deep cryptographic expertise. The simplicity and strong security guarantees of XChaCha20-Poly1305 make it a reliable alternative to AES for many applications, especially where simplicity and robustness are paramount.
