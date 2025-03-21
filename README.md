John the Ripper - Password Cracking Project
Overview
John the Ripper (JtR) is an open-source password cracking tool. This project shows how to use JtR in a Linux terminal to crack a hashed password.

Installation
Update your system and install John the Ripper by running:
sudo apt update
sudo apt install john -y

Verify the installation with:
john --version

Creating a Hashed Password
Generate a SHA-512 hashed password and save it to a file:
echo -n "password123" | openssl passwd -6 > hashes.txt

View the hash:
cat hashes.txt

Cracking the Password
Run John the Ripper on the hash file:
john hashes.txt

Viewing the Cracked Password
After John finishes, display the cracked password:
john --show hashes.txt

Using a Custom Wordlist (Optional)
If John cannot crack the password, use a larger wordlist:
john --wordlist=/usr/share/wordlists/rockyou.txt hashes.txt

Make sure rockyou.txt is installed by running:
sudo apt install wordlists

Conclusion
You have successfully used John the Ripper to crack a hashed password in a Linux terminal.

