
# 🔐 John the Ripper - Password Cracking Project

**John the Ripper (JtR)** is an open-source password cracking tool used to test password strength and recover lost credentials.  
This project demonstrates how to use JtR in a Linux terminal to crack a SHA-512 hashed password.

---

## 🛠️ Installation

Update your system and install John the Ripper:

```bash
sudo apt update
sudo apt install john -y
```

Verify the installation:

```bash
john --version
```

---

## 🔒 Creating a Hashed Password

Generate a SHA-512 hashed password and save it to a file:

```bash
echo -n "password123" | openssl passwd -6 > hashes.txt
```

View the hash:

```bash
cat hashes.txt
```

---

## 🧠 Cracking the Password

Run John the Ripper on the hash file:

```bash
john hashes.txt
```

---

## 🔓 Viewing the Cracked Password

After John finishes:

```bash
john --show hashes.txt
```

---

## 📁 Using a Custom Wordlist (Optional)

If John is unable to crack the password with the default list, use a larger wordlist:

```bash
john --wordlist=/usr/share/wordlists/rockyou.txt hashes.txt
```

Make sure `rockyou.txt` is installed:

```bash
sudo apt install wordlists
```

---

## ✅ Conclusion

You have successfully used **John the Ripper** to crack a hashed password in a Linux terminal.  
This project helps demonstrate real-world password security and highlights the importance of strong, unpredictable credentials.

---

> 🔗 **Note:** Use this tool ethically and only for educational or authorized security testing purposes.
