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

# Usage

1. **Run the script by passing the passwords you want to check as command-line arguments.**

   ```bash
   python pwned_password_checker.py [password1] [password2] ...

2. **Exampl**
   ```bash
   python pwned_password_checker.py password123 qwerty mySecurePass!

3. **Sample Output:**
   ```bash
   password123 was found 738,279 times. Change your password!
   qwerty was found 1,011,556 times. Change your password!
   mySecurePass! was not found!

#### Note: Be cautious when entering your passwords in the command line, as they might be stored in your shell history.

# How It Works

## Hashing the Password
- The script converts your password into a SHA-1 hash.
- Example: password123 becomes CBFDAC6008F9CAB4083784CBD1874F76618D2A97.
## Using k-Anonymity
- Sends the first 5 characters of the hash to the API.
- Example: Sends CBFDA to the API.
## Receiving Potential Matches
- The API returns a list of hashes that match the first 5 characters.
- The script compares the returned hashes with your full hash.
## Reporting the Results
- If a match is found, it reports how many times the password has appeared in breaches.
- If no match is found, it indicates that your password was not found.
## Security Considerations
- Privacy: Your full password or full hash is never sent over the network.
- Local Execution: All sensitive computations are done locally on your machine.
- Caution: Avoid running this script on untrusted machines or sharing your passwords.

# License

This project is licensed under the MIT License. See the LICENSE file for details.

# Acknowledgments

- Have I Been Pwned: Thanks to Troy Hunt for providing the [Have I Been Pwned](https://haveibeenpwned.com/).
- Community: Inspired by the need for better personal cybersecurity practices.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements.

## Contact
For questions or suggestions, feel free to open an issue or contact me directly.
