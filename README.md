Transaction Id: at1hnnlruqc67fuh49lucj87qjt8kzaw2hccegs6jxg93mncp2lysrsm2plq3

# Privacy Compliance Token

## Description
The **Privacy Compliance Token** is designed to enforce data privacy regulations by allowing only approved recipients to access certain transactions or sensitive data. The smart contract ensures compliance by maintaining an `approved_recipients` list, restricting unauthorized access, and providing transparency in privacy-based interactions.

## How It Works
- The contract maintains a **mapping of approved recipients**.
- Before performing any operation requiring privacy compliance, the contract **checks if the recipient is approved**.
- If the recipient is **not approved**, the operation is rejected.
- If the recipient is approved, the transaction or data-sharing process proceeds.
- The contract **enables administrators** to modify the list of approved recipients as needed to ensure compliance with regulations.

### Intended Use Case
This token is particularly useful for:
- **Regulated financial transactions** where only authorized institutions can receive payments.
- **Privacy-focused data sharing** in healthcare, legal, and enterprise environments.
- **Secure on-chain access control** for blockchain-based applications requiring compliance verification.

## Deployment Instructions

### Prerequisites
Ensure you have the following installed:
- [Leo](https://developer.aleo.org/) programming language
- Aleo CLI for building and deploying smart contracts
- A valid Aleo account

### Steps to Deploy
1. **Clone the repository:**
   ```sh
   git clone https://github.com/DevBig-Tee/Privacy-compliance_token.git
   cd Privacy-compliance_token
   ```
2. **Build the smart contract:**
   ```sh
   leo build
   ```
3. **Run tests (optional but recommended):**
   ```sh
   leo test
   ```
4. **Deploy the contract to the Aleo network:**
   ```sh
   leo deploy
   ```
5. **Interact with the contract:**
   - Add an approved recipient:
     ```sh
     leo run add_recipient <recipient_address>
     ```
   - Verify recipient approval status:
     ```sh
     leo run is_approved <recipient_address>
     ```
   - Execute a privacy-compliant transaction:
     ```sh
     leo run transfer <recipient_address> <amount>
     ```

## Contributing
Contributions are welcome! Please submit a pull request or open an issue for any improvements or bug fixes.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---
For any inquiries or issues, please contact [DevBig-Tee](https://github.com/DevBig-Tee).

