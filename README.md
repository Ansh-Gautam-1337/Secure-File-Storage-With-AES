# 🔐 Secure File Storage System

![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)
![Platform](https://img.shields.io/badge/platform-windows%20%7C%20linux%20%7C%20macos-lightgrey)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-stable-brightgreen)

A cross-platform **GUI + CLI-based file encryption and decryption tool** that provides **military-grade security** using AES-256 encryption, SHA-256 hashing for file integrity, and PBKDF2 key derivation with salt protection.

Developed with 💙 PyQt5 for the GUI and Python's `cryptography` library for secure backend logic.

---

## 🚀 Features

- 🔒 **AES-256 CBC Encryption** using PBKDF2-derived keys
- 🧂 **Salted Key Derivation** for strong password protection
- 🔑 **Fernet Encryption** for secure metadata and data handling
- 🛡️ **SHA-256 Hashing** for file integrity verification
- 📁 **Metadata Generation** (timestamp, original filename, hash, size)
- 🧠 **Threaded GUI** with real-time progress and responsive interaction
- 📤 **Encrypted file & metadata storage** with `.enc` and `.meta` extensions
- 🖥️ **Dual Interface**: CLI for power users, GUI for simplicity
- 💾 **Persistent Secure Storage Directory**
- 📓 **Logging** of encryption/decryption events for auditing

---

## 🖼️ GUI Preview

> GUI includes two tabs: Encrypt & Decrypt with:
- File Browsing
- Password Fields
- Progress Bar
- Status Console Output

---

## 🛠️ Installation

### 1. Clone the repository
```bash
git clone https://github.com/Ansh-Gautam-1337/Secure-File-Storage-With-AES.git
cd Secure-File-Storage-With-AES
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

> ✅ Requirements:
> - Python 3.8+
> - PyQt5
> - cryptography

---

## 🧑‍💻 How to Use

### 🔷 GUI Mode (Recommended)

```bash
python Secure_File_Storage_With_AES_Encryption.py
```

- Launches an intuitive interface
- Select a file, enter a password, and encrypt or decrypt with progress

### 🔷 CLI Mode (Advanced)

#### 🔐 Encrypt a File
```bash
python Secure_File_Storage_With_AES_Encryption.py --encrypt path/to/file.txt
```

#### 🔓 Decrypt a File
```bash
python Secure_File_Storage_With_AES_Encryption.py --decrypt path/to/file.enc --output decrypted_dir/
```

You will be prompted to enter a password in both cases.

---

## 📂 File Structure

```
📁 SecureStorage/
├── .salt                  # Salt used for PBKDF2 key derivation
├── 1728393283.enc         # Encrypted file
├── 1728393283.meta        # Encrypted metadata
├── secure_storage.log     # Log file for all operations
```

---

## ⚙️ Internals

### 🔐 Cryptographic Details
- **AES-256-CBC** with random IV
- **PBKDF2HMAC** using SHA-256 with 100,000 iterations
- **Salted keys** stored securely
- **File hash** verified after decryption for tamper detection

### 🧠 Multithreading
- All operations run in background threads to avoid UI freeze
- Real-time progress updates in GUI

---

## 📝 Logging

All operations (success/failure) are logged in `secure_storage.log` with timestamps for traceability.

---

## ✅ Use Cases

- Secure file backups
- Portable encrypted data transfers
- Educational tool for cryptography learners
- Internal file auditing for organizations

---

## 🙌 Contribution

Feel free to submit issues or PRs to improve this tool.

---

## 📜 License

This project is licensed under the **MIT License** - do whatever you want but don't blame us! 😄

---

## 🤝 Credits

Developed with ❤️ using:
- [PyQt5](https://pypi.org/project/PyQt5/)
- [cryptography](https://pypi.org/project/cryptography/)
- Python's `hashlib`, `argparse`, and standard libraries

---

## 🔗 Related Projects

- 🔐 [cryptography](https://github.com/pyca/cryptography)
- 💾 [PyInstaller](https://github.com/pyinstaller/pyinstaller)

---
