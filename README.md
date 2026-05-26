# 🔒 secret-cipher-py

A lightweight Python script to easily encode and decode secret messages using a custom text cipher.

## ✨ Features
* **Dual Modes**: Easily toggle between **Coding** (Encryption) and **Decoding** (Decryption).
* **Smart Padding**: Words with 2 or more characters are heavily masked using prefix/suffix padding and character rotation.
* **Single-Char Safety**: Words with fewer than 2 characters are safely reversed to maintain layout integrity.
* **Zero Dependencies**: Runs entirely on pure, native Python.

## 🚀 How It Works

### 1. Encryption Rule (`coding = True`)
If a word contains **2 or more characters**:
1. The first letter is moved to the very end of the word.
2. Three padding characters (`dsf`) are added to the beginning.
3. Three padding characters (`jkr`) are added to the end.

*Example:* `python` ➡️ `dsf` + `ython` + `p` + `jkr` ➡️ **`dsfythonpjkr`**

If a word contains **1 character**, it is simply reversed.

### 2. Decryption Rule (`coding = False`)
The exact inverse operation is performed:
1. Strips the 3 padding characters from the front and back.
2. Takes the last letter and moves it back to the very front.

---

## 🛠️ Usage

### Prerequisites
Make sure you have [Python 3.x](https://python.org) installed.

### Running the Script
1. Clone this repository to your machine.
2. Open the script file and set your mode:
   ```python
   coding = True   # Set to True to encrypt, False to decrypt
   ```
3. Execute the script in your terminal:
   ```bash
   python cipher.py
   ```

---

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to fork the project and submit a pull request.

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).
