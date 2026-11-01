# ALM-2 — AES Client-Server File Transfer

**Student:** Aryan Sonak  
**Roll Number:** 2420090049  
**Section:** 11

## Objective

This project uses AES encryption to transfer text files between a Python client and server. The client sends a 10 KB text file to the server, and the server sends a different 5 KB text file back to the client.

## Technologies Used

- Python 3
- TCP sockets
- PyCryptodome
- AES-128 in CBC mode

## How It Works

AES encrypts the file contents before they are sent through the TCP connection. A random initialization vector (IV) is generated for each encryption, and PKCS#7 padding is used to fit the data into AES blocks.

The transfer takes place in two directions:

1. **Client to server:** the client reads `files/client/sample_10kb.txt`, encrypts it and sends it to the server. The server decrypts and saves the file.
2. **Server to client:** the server reads `files/server/sample_5kb.txt`, encrypts it and sends it back. The client decrypts and saves the file.

The received files are checked using SHA-256 hashes.

## Project Structure

- `client.py` — client-side file encryption and transfer.
- `server.py` — receives the client file and sends the server file.
- `algorithms/` — AES encryption and decryption functions.
- `network/` — TCP communication helpers.
- `files/` — sample text files for both transfer directions.
- `received/` — files received by the client and server.
- `tests/` — tests for AES and file transfer.

## Requirements

- Python 3.9 or later
- PyCryptodome

Install the required library:

```bash
python -m pip install pycryptodome
```

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

Follow the prompts in the client terminal to start the transfer.

## Testing

Run the tests from this folder:

```bash
python -m unittest discover -s tests -v
```
