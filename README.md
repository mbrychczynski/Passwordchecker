# Pwned Password Checker

A simple Python script to check if your passwords have been compromised in data breaches using the [Have I Been Pwned](https://haveibeenpwned.com/) Pwned Passwords API.

## Description

This script allows you to securely check whether your passwords have appeared in any known data breaches. It leverages the Pwned Passwords API, which uses a k-Anonymity model to protect the privacy of the passwords being checked. Only a partial hash of your password is sent to the API, ensuring that your actual password remains secure.

## Features

- **Secure Password Checking**: Uses SHA-1 hashing and the k-Anonymity model to ensure your passwords are not exposed.
- **Data Breach Count**: Reports the number of times your password has appeared in breaches.
- **Easy to Use**: Simple command-line interface for quick checks.

## Requirements

- Python 3.x
- `requests` library

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/pwned-password-checker.git
   
2. **Navigate to the Directory**
    ```bash
    cd pwned-password-checker

3. **Install Dependencies**
    ```bash
   pip install requests
