# Hashcat – Advanced Hash Cracking

Hashcat is a **high-performance hash cracking tool**
(commonly GPU-based).

---

## 🔹 Why Hashcat needs TXT file?
- Hashcat reads hashes from files
- Supports multiple hashes at once
- Faster and more flexible attacks

---

## 🔹 Basic Syntax
hashcat -m <hash_type> -a <attack_mode> hashes.txt wordlist.txt

---

## 🔹 Common Examples

### MD5 Dictionary Attack
hashcat -m 0 -a 0 hashes.txt rockyou.txt

### NTLM Hash
hashcat -m 1000 -a 0 hashes.txt rockyou.txt

---

## 🔹 Mask Attack (Bruteforce Pattern)
hashcat -m 0 -a 3 hashes.txt ?a?a?a?a?a?a

---

## 🔹 Hybrid Attack
hashcat -m 0 -a 6 hashes.txt rockyou.txt ?d?d

---

## 🔹 Show Cracked Passwords
hashcat -m 0 hashes.txt --show

---

## 🔹 Common Attack Modes
0 → Dictionary  
3 → Mask  
6 → Wordlist + Mask  

---

## 🔹 Notes
- Faster than John
- Requires correct hash mode
- Used in **professional pentesting**
