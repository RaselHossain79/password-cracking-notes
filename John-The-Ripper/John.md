# John the Ripper – Offline Password Cracking

John is used for **cracking password hashes** extracted from files.

---

## 🔹 Why hashes are saved in .txt?
- John reads hashes only from text files
- One hash per line
- Standard pentesting practice

---

## 🔹 Creating Hash File
nano hashes.txt

Example:
5f4dcc3b5aa765d61d8327deb882cf99

---

## 🔹 Basic Cracking
john hashes.txt

---

## 🔹 Using Wordlist
john --wordlist=rockyou.txt hashes.txt

---

## 🔹 Show Cracked Passwords
john --show hashes.txt

---

## 🔹 Specify Hash Format
john --format=md5crypt hashes.txt

---

## 🔹 Extracting Hashes from Files

### ZIP File
zip2john secret.zip > ziphash.txt
john ziphash.txt

### PDF File
pdf2john file.pdf > pdfhash.txt
john pdfhash.txt

### RAR File
rar2john secret.rar > rarhash.txt
john rarhash.txt

### Office File (Word / Excel)
office2john file.docx > officehash.txt
john officehash.txt

### Linux Password Hash
unshadow /etc/passwd /etc/shadow > linuxhash.txt
john linuxhash.txt

---

## 🔹 Notes
- John is best for **simple & medium strength hashes**
- Easy to use
- Very common in CTF & exams
