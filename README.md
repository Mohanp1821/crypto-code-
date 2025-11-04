# 🔐 Caesar Cipher Encryption using Python

## 📘 Project Overview
This project demonstrates the implementation of the **Caesar Cipher**, one of the oldest and simplest encryption algorithms, using **Python**.  
It allows a user to enter a word and a shift value, then generates an encrypted (ciphered) version of the input word.

---

## 🧠 What is the Caesar Cipher?
The **Caesar Cipher** is a substitution cipher that shifts each letter in the plaintext by a fixed number of positions down the alphabet.

For example:
```
Plaintext : HELLO
Shift     : 3
Ciphertext: KHOOR
```

Mathematically:
```
C = (P + K) mod 26
```
where:
- **C** → Ciphertext letter  
- **P** → Plaintext letter (0–25)  
- **K** → Shift value

---

## 💻 Python Code
```python
import string
word = input("enter a word: ")

def caesar_cipher(password, shift):
    """Applies a Caesar cipher to a given password."""
    cipher = ""
    for ch in password:
        if ch.isalpha():  # only letters
            start = ord('a') if ch.islower() else ord('A')
            new_char = chr(((ord(ch) - start + shift) % 26) + start)
            cipher += new_char
        else:
            cipher += ch  # keep spaces, numbers, etc. same
    return cipher
    
shift = int(input("enter the shift number:"))

generated_password = word
ciphered_password = caesar_cipher(generated_password, shift)

print("Generated Password:", generated_password)
print("Ciphered Password:", ciphered_password)
```

---

## ⚙️ How It Works
1. The program takes a **word** as input from the user.  
2. The user provides a **shift number** (how many letters to shift).  
3. Each letter is replaced by another letter based on the shift value.  
4. The output displays both the original and encrypted password.

---

## 🧩 Example Output
```
enter a word: hello
enter the shift number: 3
Generated Password: hello
Ciphered Password: khoor
```

---

## 📚 Python Concepts Used
- **Functions (`def`)**
- **Loops (`for` loops)**
- **Conditionals (`if-else` statements)**
- **String Handling (`isalpha()`)**
- **ASCII Conversions (`ord()` and `chr()`)**
- **Modular Arithmetic (`% 26`)**

---

## 🚀 Applications
- Basic encryption demonstrations  
- Learning tool for classical cryptography  
- Educational programming exercises  

---

## ⚠️ Limitations
- Not suitable for modern encryption (easily breakable).  
- Only supports alphabetic characters; others remain unchanged.  
- Vulnerable to frequency analysis attacks.  

---

## 🧑‍🎓 Author
**Student 1234**  
BBA-AI, Symbiosis  
GitHub: [Your GitHub Profile Link Here]

---

## 📄 License
This project is open-source and free to use for educational purposes.
