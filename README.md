# Personal Financial Statement Generator

A simple, local, browser-based Personal Financial Statement (PFS) generator built in HTML and JavaScript. I built this tool because I hate filling out Personal Financial Statements every time we need financing for a project or when a bank requires one for mortgage compliance. I also prefer keeping my sensitive data local and away from the cloud.

## Why I Built It

- **Reduce Repetitive Work:** No more manually filling out PFS forms every time financing is needed.
- **Privacy:** Data is stored locally so your personal information never leaves your machine unless you explicitly export it.
- **Fun & Practical:** A project to serve a need and push the possibilities with ChatGPT.
- **Rapid Development:** Built in an hour based on screenshots of bank PFS forms, proving that simple tools can be highly effective.

## Features

- **Local & Simple:** Runs entirely in your browser using HTML and JavaScript—no backend required.
- **Dynamic Form Fields:** Easily add or remove rows for various sections such as Assets, Liabilities, Annual Income, Annual Expenditures, and more.
- **Personal Information:** Detailed fields for both Applicant and Co-Applicant, including home address, years at address, and date of birth.
- **Contingent Liabilities & Additional Questions:** Answer yes/no questions and open-ended queries as needed.
- **JSON Save/Import with Optional Encryption:** Save your data locally as JSON (encrypted with AES-GCM if desired) so you can import and update it later.
- **PDF Export:** Generate a professional, read-only PDF of your Personal Financial Statement for presentations or mortgage compliance.
- **Local Deployment:** Run the app locally using a simple command like `npx http-server .`.

## Getting Started

### Prerequisites

- A modern web browser
- [Node.js](https://nodejs.org/) installed (for running a local server)

### Running Locally

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/yourrepo.git
   cd yourrepo

2. **Run a Local Server:**
   ```bash
   npx http-server .

3. **Open the App:**
   Visit http://localhost:8080 (or the port provided by your server) in your browser.

## Optional Encryption for JSON Export/Import

The tool uses the Web Crypto API (AES-GCM) to optionally encrypt your JSON data on export. When exporting, you’ll be prompted for a password; if you provide one, your data will be encrypted. On import, the tool first attempts to read the file as unencrypted JSON, and if that fails, it prompts for a password to decrypt the file.

### Encryption & Decryption Logic

The encryption is based on PBKDF2 to derive an AES-GCM key from your password. The exported file (if encrypted) contains a base64-encoded string combining a random salt, IV, and ciphertext.

For a detailed look at the code, please see the source comments.

## License

This project is open source under the MIT License.

If you use this software in any commercial project, please provide attribution to the Bret Morgan Group.

Copyright (c) 2025 Bret Morgan

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Summary

This Personal Financial Statement Generator is a lightweight, local tool to quickly generate, save, and export your financial data without exposing it to the cloud. Enjoy a practical solution to reduce repetitive tasks and keep your data secure!

Built with an interactive dialogue with ChatGPT to push the current possibilities of local, disposible, open-source tools.open .