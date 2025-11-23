# 🛡️ Multi‑Service Credential Validator for Security Auditing (C++)

This C++ tool is designed for **bulk credential validation** during security audits and penetration testing engagements.  
It processes large lists of hosts and credentials, then checks access across multiple services such as **SSH (22)**, **cPanel (2083)**, and **WebMail (2084)**.  
All results are stored neatly inside the `result/` directory for reporting or follow‑up analysis.

> ⚠️ This tool is intended for **authorized security testing only** (penetration testing, internal audits, red/blue team automation).

---

## 🔐 Cybersecurity Use Cases

- **Internal credential audits**
- **Misconfiguration & weak password detection**
- **Asset validation during pentests**
- **Infrastructure exposure assessment**
- **Mass service accessibility checking**
- **Compliance verification (CIS, NIST, ISO‑27001)**

---

## 🚀 Features

- Reads credentials from `list.txt` in the format:  
```

site.com:port:username:password

````
- Checks multiple services:
- **SSH** – Port 22  
- **cPanel** – Port 2083  
- **WebMail** – Port 2084  
- High‑speed processing optimized with C++
- Organized results saved to:
- `result/ssh.txt`
- `result/cpanel.txt`
- `result/webmail.txt`
- `result/failed.txt`
- Designed for massive lists (scalable & efficient)
- Useful for SOC teams, sysadmins, pentesters, and auditors

---

## 📦 Installation & Compilation

### Prerequisites
- C++ compiler (`g++` recommended)
- Standard C++ libraries

### Compile
```sh
g++ -o multi_checker 1.cpp
````

---

## 🧪 Usage

### 1. Create `list.txt`

Format:

```
example.com:22:user1:password123
myserver.net:2083:admin:securepass
demo.org:2084:test:12345
```

### 2. Run the Tool

```sh
./multi_checker
```

### 3. Results

Saved in the `result/` folder:

* `result/ssh.txt`
* `result/cpanel.txt`
* `result/webmail.txt`
* `result/failed.txt`

This makes the tool suitable for generating **audit reports**, **pentest documentation**, and **security validation logs**.

---

## ⚙️ Technical Notes

* The current version **simulates** connection checking for demonstration.
* To enable real credential validation, extend the functions:

  * `check_ssh_connection()`
  * `check_cpanel_connection()`
  * `check_webmail_connection()`
* Ensure all tests comply with law and client authorization.

---

## ⚠️ Legal Disclaimer

Unauthorized access to systems is **illegal**.
This project is created for **educational and authorized security testing only**.

---

## 🤝 Contributing
```
Pull requests and improvements are welcome to expand protocol support or improve efficiency.

```
