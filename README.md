
# 🛡️ Injectra

Injectra is a CLI-based payload generator and vulnerability testing toolkit designed for penetration testers and bug bounty hunters. It supports XSS, SQL Injection, and Command Injection vectors with payload customization, encoding options, and export features.


## 📦 Features

- 🔍 XSS Module
  - Reflected, Stored, DOM-Based & Evasion payloads
  - Payload encoding: Base64, URL, Unicode
  - Export payloads to `.json` 

- 💉 SQL Injection Module
  - Error-Based, Union-Based, Blind & WAF Bypass payloads
  - Payload testing on target URLs
  - Multiple encodings supported

- 🖥️ Command Injection Module
  - Linux & Windows payloads
  - Encoding & obfuscation options
  - Clipboard support & export formats


## 🚀 Usage

bash

python main.py --xss --target https://example.com

python main.py --sqli --target https://example.com --param id --type error --encode base64

python main.py --cmdinj --os linux --encode url --obfuscate



## 🎯 Flags & Parameters

### XSS

| Flag         | Description                                              |
| ------------ | -------------------------------------------------------- |
| `--xss`      | Run the XSS module                                       |
| `--xss-type` | XSS types: `reflected`, `stored`, `dom`, `all`, `bypass` |
| `--encode`   | Encode payloads: `base64`, `url`, `unicode`              |
| `--target`   | (Optional) Show target in logs                           |



### SQL Injection

| Flag        | Description                                    |
| ----------- | ---------------------------------------------- |
| `--sqli`    | Run the SQL Injection module                   |
| `--target`  | Target URL (required for scanning)             |
| `--param`   | GET parameter to test (default: `id`)          |
| `--type`    | Payload type: `error`, `union`, `blind`, `all` |
| `--encode`  | Encoding method                                |
| `--keyword` | Optional keyword to detect in response         |



### Command Injection

| Flag          | Description                          |
| ------------- | ------------------------------------ |
| `--cmdinj`    | Run the Command Injection module     |
| `--os`        | Target OS: `linux`, `windows`, `all` |
| `--encode`    | Encoding method                      |
| `--obfuscate` | Use `${IFS}` obfuscation             |
| `--export`    | Output format: `cli`, `json`         |
| `--copy`      | Copy output to clipboard             |



## 🖼️ Screenshots



### XSS Payload Generation


![XSS 1](https://github.com/user-attachments/assets/8a234239-92a0-437d-9634-8f3e36b1b529)


![XSS 2](https://github.com/user-attachments/assets/062c64a9-ea07-4437-9c11-b5622d0e6181)


### SQL Injection Scanning


![SQL 1](https://github.com/user-attachments/assets/d3cb010d-e930-433b-867b-b950418ca4fc)


![SQL 2](https://github.com/user-attachments/assets/984e345a-1b87-4487-a1fe-e538b9ea80d7)


![SQL 3](https://github.com/user-attachments/assets/7c0b8080-92c6-4b66-8b59-645797e14b1d)



### Command Injection Generation


![Cmd Injec tion 1](https://github.com/user-attachments/assets/06c2b1a2-698d-4e30-8768-ccaa290c5e05)


![Cmd Injection 2](https://github.com/user-attachments/assets/dceac7e8-66a2-4efb-933b-4486eb1483b9)


## 🧰 Requirements

Install dependencies using:

pip install requests pyperclip



## ⚠️ Disclaimer

This tool is intended for educational and authorized testing only. Using it on unauthorized targets is illegal.


