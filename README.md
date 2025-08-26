# LiteCrypt  

**LiteCrypt** is a lightweight educational block cipher for **file encryption and decryption**. Inspired by AES, it uses 2-byte blocks with nibble substitution, row shifts, MixColumns in GF(2⁴), and a simple key schedule.  

⚠️ This project is for learning purposes only.  

---

## 🔧 Features  
- File **encryption and decryption** with a toy block cipher  
- Operates on **2-byte blocks** (4 nibbles)  
- **S-Box / inverse S-Box** for confusion  
- **ShiftRows** and **MixColumns** for diffusion  
- Simple **key schedule** with 2 rounds  
- Clear and modular code (`fun.c/.h`, `encrypt.c`, `decrypt.c`)  

---

## 📂 Project Structure  
├── encrypt.c # File encryption driver
├── decrypt.c # File decryption driver
├── fun.c # Core functions (S-Box, MixColumns, key schedule, etc.)
└── fun.h # Function declarations


---

## 🚀 Build & Run  

### Compile
```bash
gcc encrypt.c fun.c -o encrypt
gcc decrypt.c fun.c -o decrypt

./encrypt input.txt encrypted.bin
./decrypt encrypted.bin output.txt
```

##📖 Notes

Works on 2-byte blocks, so padding is applied implicitly when the file size is not aligned.

Key is currently hardcoded inside encrypt.c and decrypt.c. You can modify it in the code for custom runs.

Designed for educational demonstration of block cipher concepts, not secure encryption.
