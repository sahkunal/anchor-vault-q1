# 🔐 Anchor Vault Program

![Solana](https://img.shields.io/badge/Solana-Program-14F195?style=for-the-badge\&logo=solana\&logoColor=black)
![Anchor](https://img.shields.io/badge/Framework-Anchor-512DA8?style=for-the-badge)
![Rust](https://img.shields.io/badge/Rust-Program-000000?style=for-the-badge\&logo=rust)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

A **Solana vault smart contract** built using the Anchor framework.
This project demonstrates secure instruction handling, transaction execution, and structured development workflows for on-chain programs.

---

## 📌 Overview

The Anchor Vault Program showcases:

* Writing Solana smart contracts with Anchor
* Program deployment and upgradeability
* Instruction execution and logging
* Anchor-based testing workflows

This repository is designed to remain **RPC-agnostic**, allowing deployment across different environments without code changes.

---

## 🧱 Architecture

```
Client (Tests / Scripts)
        │
        ▼
Anchor Program (Vault Logic)
        │
        ▼
Solana Runtime
```

### Core Components

* **Program Instructions**

  * Initialize vault
  * Submit transactions
  * Handle account interactions

* **Accounts**

  * Vault state accounts
  * User accounts
  * System program integrations

---

## 📂 Project Structure

```
anchor-vault-q1/
│
├── programs/
│   └── anchor_vault_q1/
│       └── src/
│           └── lib.rs
│
├── tests/
│   └── *.ts
│
├── Anchor.toml
├── package.json
└── tsconfig.json
```

---

## ⚙️ Prerequisites

Install required tooling:

* Solana CLI
* Anchor Framework
* Rust toolchain
* Node.js + Yarn

Verify installation:

```bash
solana --version
anchor --version
rustc --version
```

---

## 🛠 Configuration

Project configuration lives in:

```
Anchor.toml
```

You may configure any desired cluster without modifying program logic.

Example:

```toml
[provider]
cluster = "localnet"
wallet = "~/.config/solana/id.json"
```

---

## 🚀 Build the Program

Compile the smart contract:

```bash
anchor build
```

Artifacts will appear in:

```
target/deploy/
```

---

## 📦 Deploy the Program

```bash
anchor deploy
```

Verify deployment:

```bash
solana program show <PROGRAM_ID>
```

Expected indicators:

* Executable: Yes
* Upgradeable: Yes

---

## 🧪 Run Tests

```bash
anchor test
```

This command:

* Deploys the program
* Executes test scripts
* Prints program logs

---

## 🔎 Debugging & Logs

View live program logs:

```bash
solana logs
```

Example instruction output:

```
Program log: Instruction: Submit
```

Inspect a transaction:

```bash
solana confirm <SIGNATURE> -v
```

---

## 🔐 Vault Flow (Conceptual)

```
User → Submit Instruction → Vault Program → State Update → Logs
```

1. User sends transaction
2. Anchor validates accounts
3. Vault logic executes
4. Program emits logs
5. Transaction finalized

---

## 📊 Development Notes

* Instruction decoding may vary depending on explorer and cluster.
* CLI logs provide the most reliable debugging during development.
* Anchor automatically logs instruction names via the `#[program]` macro.

---

## 📚 Useful Commands

```bash
anchor build
anchor deploy
anchor test
solana logs
solana confirm <SIGNATURE> -v
```

---

## 🤝 Contributing

Contributions are welcome.
Feel free to open issues or submit pull requests.

---

## 📄 License

MIT License

---
