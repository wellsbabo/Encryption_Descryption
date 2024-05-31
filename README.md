# AES128 Encryption/Decryption GUI

This Python application provides a graphical user interface (GUI) for encrypting and decrypting data using AES128/ECB/PKCS7Padding. It supports both URL-safe encoding and decoding. The application is built using `tkinter` and `cryptography` libraries.

## Development motivation

I developed an API server that encrypts values ​​and sends back encrypted responses. In addition to simple encryption and decryption, if the time in the data differs by more than 5 minutes from the current time, it is treated as an invalid value. So, I created this program because it was annoying to encrypt and decrypt by changing the time of the value every time.

## Features

- **Encrypt Data**: Encrypt plain text or JSON data with a 16-byte key.
- **Decrypt Data**: Decrypt AES128 encrypted data with the same 16-byte key.
- **Update `createdAt`**: Decrypt data, update the `createdAt` field to the current time, and re-encrypt it.
- **Add `createdAt`**: Optionally add a `createdAt` field with the current time when encrypting data.
- **Copy to Clipboard**: Easily copy the encrypted or decrypted results to the clipboard.

## Installation

1. **Clone the repository**:
    ```sh
    git clone https://github.com/yourusername/AES128-Encryption-Decryption-GUI.git
    cd AES128-Encryption-Decryption-GUI
    ```

2. **Install the required packages**:
    ```sh
    pip install cryptography
    ```

3. **Run the application**:
    ```sh
    python app.py
    ```

## Usage

1. **Encryption**:
    - Enter a 16-byte key.
    - Enter the data to be encrypted (plain text or JSON).
    - Select the request type (GET or POST).
    - Optionally check the "Add createdAt" checkbox to add a `createdAt` field with the current time.
    - Click the "Encrypt" button to encrypt the data.
    - The encrypted data will be displayed in the "Encrypted Data" section.
    - The original data or updated data (with `createdAt` field) will be displayed in the "Decrypted Data" section.
    - Click the "Copy Encrypted Data" button to copy the encrypted data to the clipboard.
    - Click the "Copy Decrypted Data" button to copy the decrypted data to the clipboard.

2. **Change Time**:
    - Enter a 16-byte key.
    - Enter the encrypted data.
    - Select the request type (GET or POST).
    - Click the "Change Time" button to decrypt the data, update the `createdAt` field to the current time, and re-encrypt the data.
    - The updated encrypted data will be displayed in the "Encrypted Data" section.
    - The decrypted data with the updated `createdAt` field will be displayed in the "Decrypted Data" section.

3. **Decryption**:
    - Enter a 16-byte key.
    - Enter the encrypted data to be decrypted.
    - Click the "Decrypt" button to decrypt the data.
    - The decrypted data will be displayed in the "Decrypted Result" section.
    - Click the "Copy Decrypted Result" button to copy the decrypted data to the clipboard.

## Changelog

### [1.0.0] - 2024-05-28
#### Added
- Initial release with encryption and decryption functionality.
- Support for GET and POST request types.
- Feature to update `createdAt` field to current time and re-encrypt data.
- Copy to clipboard functionality for both encrypted and decrypted data.
- "Add createdAt" checkbox to optionally add a `createdAt` field with the current time during encryption.
- Improved error handling and messages for decryption and JSON parsing.

## License

This project is licensed under the MIT License.
