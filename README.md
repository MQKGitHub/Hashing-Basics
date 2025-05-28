### 🛡️ Hashing Basics

**Room:** [Hashing Basics — TryHackMe](https://tryhackme.com/room/hashingbasics)  
**Status:** ✅ Completed  
**Date:** *28 May 2025* 

---

### 🎯 Objective  
To understand how hashing works, how it's used in authentication and integrity checking, and how to recognise, store, and crack hashed passwords.  

---

### 🗝️ Key Concepts  
- **Hash Function** — A one-way function that converts any input into a fixed-length output (digest).  
- **Hash Value** — The unique string produced by a hash function.  
- **Hash Collision** — When two different inputs produce the same hash output (undesirable).  
- **Salt** — A random value added to passwords before hashing to prevent rainbow table attacks.  
- **Rainbow Table** — A lookup table of precomputed hashes used to reverse weak, unsalted hashes.  
- **HMAC** — A keyed-hash message authentication code that ensures both integrity and authenticity.  
- **Encoding vs Encryption vs Hashing** — Encoding changes format, encryption secures data and is reversible, hashing is one-way and used for verification.  
- **yescrypt / bcrypt / scrypt / Argon2** — Secure password hashing algorithms designed to resist cracking.  
- **/etc/shadow** — A Linux file that securely stores password hashes (not viewable by regular users).  
- **Hashcat** — A powerful tool used for password cracking using GPUs.  

---

### 🛠️ Tools Used  
- **hashcat** — Used to crack hashes using wordlists like rockyou.txt.  
- **John the Ripper** — Mentioned as a CPU-based password cracker for use in VMs.  
- **sha256sum / sha1sum / md5sum** — Used to calculate and compare hash values for files.  
- **base64** — Used to encode/decode strings (useful for understanding data encoding).  
- **hexdump** — Used to view binary data and compare files bit-by-bit.  

---

### ⚠️ Challenges Faced  
- Keeping track of different hashing algorithms and their formats (MD5, SHA1, bcrypt, yescrypt).  
- Understanding where and how salts are stored and used in hashed passwords.  
- Confusing rainbow tables with brute-force cracking — needed examples to properly understand the difference.

---

### 🧠 What I Learned  
- The structure of Linux shadow hashes (`$algorithm$salt$hash`) and how to identify the hash type.  
- Why salts are essential in secure password storage.  
- That cracking salted hashes requires tools like Hashcat or John with the correct wordlist and algorithm ID.  
- How to verify file integrity using hashes and why it matters for large downloads and updates.  
- That some hashing algorithms like MD5 and SHA1 are now broken and shouldn't be used.

---

### 🌐 Real-World Application:  
> Hashing is everywhere — login systems use it to protect passwords, software publishers use it to verify downloads, and forensic teams use it to prove file integrity. Understanding how to recognise, store, and crack hashes is crucial for both offensive and defensive cyber security roles.

---

### 💭 Reflections:  
- This was a dense room but packed with useful information.  
- The real-world stories like the RockYou breach and LinkedIn breach made it all more memorable.  
- I now understand exactly what makes a hash secure — and why older algorithms are dangerous.  
