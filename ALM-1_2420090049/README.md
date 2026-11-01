# ALM-1 — Cryptography Client-Server Lab

**Student:** Aryan Sonak  
**Roll Number:** 2420090049  
**Section:** 11

## Objective

This project demonstrates classical encryption, Simplified DES and communication between a Python client and server using TCP sockets. The client provides a menu to select an algorithm, enter a message and send the encrypted data to the server.

The file-transfer option uses S-DES to send a 1 MB file from the client to the server and a 10 KB file from the server back to the client.

## Algorithms

| Algorithm | Description |
|---|---|
| Caesar Cipher | Replaces each letter with another letter a fixed number of positions away. |
| Playfair Cipher | Encrypts pairs of letters using a 5×5 key square. |
| Simplified DES (S-DES) | Encrypts 8-bit blocks using a 10-bit key. |

The implementations are in the `algorithms/` folder.

## Project Structure

- `client.py` — starts the client and displays the algorithm menu.
- `server.py` — receives encrypted messages or files and handles decryption.
- `algorithms/` — cipher implementations.
- `network/` — TCP message framing and communication helpers.
- `files/` — sample files used for the transfer demonstration.
- `tests/` — unit tests for the algorithms and transfer functions.

## Requirements

- Python 3.9 or later
- No third-party Python packages are required.

## How to Run

Open two terminals in this folder.

**Terminal 1 — start the server:**

```bash
python server.py
```

**Terminal 2 — start the client:**

```bash
python client.py
```

Choose an option from the menu and follow the instructions. Start the server before running the client.

## File Transfer

The file-transfer option performs two transfers over TCP:

1. The client encrypts and sends the 1 MB sample file to the server. The server decrypts and saves the received file.
2. The server encrypts and sends the 10 KB sample file to the client. The client decrypts and saves it.

SHA-256 hashes are used to check that the received files match the originals.

## Testing

Run the unit tests from this folder:

```bash
python -m unittest discover -s tests -v
```

The tests cover the cipher operations, message framing, file handling and data integrity checks.
