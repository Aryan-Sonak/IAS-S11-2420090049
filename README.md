# Information Assurance and Security — Coursework

**Student:** Aryan Sonak  
**Roll Number:** 2420090049  
**Section:** 11

This repository contains the practical assignments and prototype work for Information Assurance and Security. Each project is kept in a separate folder with its own instructions.

## Projects

| Folder | Project |
|---|---|
| `ALM-1_2420090049/` | Caesar Cipher, Playfair Cipher and Simplified DES with TCP client-server communication and file transfer. |
| `ALM-2_2420090049/` | AES encryption and client-server transfer of text files using PyCryptodome. |
| `ALM-2-Prototype-Sentinel_2420090049/` | Sentinel network security simulator with firewall rules, IDS alerts and anomaly detection. |
| `prototype-1_2420090049/` | Secure document transfer application with a Flask backend and TypeScript frontend. |

## Getting Started

Open the folder for the project you want to run and follow its README. Install the dependencies listed for that project before starting the client, server or web application.

## Running the Tests

Run each test suite from its project directory:

```bash
# ALM-1
python -m unittest discover -s tests -v

# ALM-2
python -m unittest discover -s tests -v

# Sentinel backend
python -m pytest -q

# prototype-1 backend
python -m pytest -q
```

For the full-stack projects, start the backend and frontend separately as explained in their respective README files.
