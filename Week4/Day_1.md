## Day 1: Simple Encryption Practice

- **Install cryptography:**
    ```sh
    pip install cryptography
    ```

- **Try encrypting a file:**
    ```python
    from cryptography.fernet import Fernet

    key = Fernet.generate_key()
    cipher = Fernet(key)

    with open('sample.txt', 'rb') as f:
        data = f.read()
    encrypted = cipher.encrypt(data)
    with open('sample_encrypted.txt', 'wb') as ef:
        ef.write(encrypted)
    ```

---
