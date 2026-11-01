# Prototype-1 — Secure File Transfer Portal

**Student:** Aryan Sonak  
**Roll Number:** 2420090049  
**Section:** 11

## Overview

This project is a web application for secure document transfer. It has a Python Flask backend and a TypeScript frontend. Users can upload documents, select an encryption method, transfer the encrypted file and decrypt it at the receiving end.

## Main Parts

- **Backend:** handles user accounts, document storage, encryption, decryption and file transfers.
- **Frontend:** provides the pages and controls used to work with documents and transfers.
- **Cryptography:** includes Caesar, Playfair, S-DES and AES-based encryption options.
- **Tests:** contains tests for the backend, cryptographic functions and transfer process.

## Run the Project

First, set up and start the backend by following `backend/README.md`. Then open `frontend/README.md` and follow its instructions to install the frontend packages and start the development server.

After both parts are running, open the local frontend address shown in the terminal and check that the backend health endpoint is responding.

## Testing

From the backend folder, install the requirements and run:

```bash
python -m pytest -q
```

The test files are stored in `backend/tests/`.
