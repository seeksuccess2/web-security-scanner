# 🛡️ Web Security Scanner

**A simple Python-based web security scanner that checks websites for missing HTTP security headers.**  
This project helps identify **potential security vulnerabilities** by scanning websites for essential security headers.

---

## 📌 Features

✔ **Scans multiple websites from a file (`urls.txt`)**  
✔ **Checks for important HTTP security headers:**  
   - `Strict-Transport-Security` (HSTS)  
   - `Content-Security-Policy` (CSP)  
   - `X-Frame-Options`  
   - `X-Content-Type-Options`  
   - `X-XSS-Protection`  
   - `Referrer-Policy`  
✔ **Logs missing headers into a structured report**  
✔ **Beginner-friendly and easy to expand**  

---

## 🛠️ Installation & Setup

### 1️⃣ **Clone the Repository**
```bash
git clone https://github.com/seeksuccess2/web-security-scanner.git
cd web-security-scanner
```

### 2️⃣ **Set Up Virtual Environment**
```bash
python -m venv venv
venv\Scripts\activate  # Windows
```
### 📌 Dependency Breakdown

This project requires multiple dependencies for core functionality, development, testing, and security analysis.

Run the following command to install all required dependencies:

```bash
pip install -r requirements.txt


```
📌 How to Install a Specific Dependency

If you need to install just one package, use:

pip install <package_name>





---

## 🚀 How to Use

### **1️⃣ Add Websites to Scan**
Edit `urls.txt` and add the list of websites you want to scan:
```
https://example.com
https://testsite.com
https://google.com
```

### **2️⃣ Run the Security Scanner**
```bash
python scripts/security_scanner.py
```

### **3️⃣ View Scan Results**
Results are saved in:
```
logs/security_scan_results.txt
```

---

## 🔍 Example Output

```plaintext
Checking https://example.com...

🌟 X-Frame-Options: DENY
🌟 X-XSS-Protection: 1; mode=block
❌ Strict-Transport-Security: MISSING - Enables HTTPS enforcement
❌ Content-Security-Policy: MISSING - Controls allowed content sources

Recommendations:
- Add `Strict-Transport-Security` header: `max-age=31536000; includeSubDomains`
- Add `Content-Security-Policy` header: `default-src 'self'`
```

---

## 📌 HTTP Security Headers Explained

| Header | Purpose |
|--------|---------|
| **Strict-Transport-Security (HSTS)** | Forces browsers to only use HTTPS |
| **Content-Security-Policy (CSP)** | Restricts allowed content sources |
| **X-Frame-Options** | Prevents clickjacking attacks |
| **X-Content-Type-Options** | Prevents MIME-type sniffing |
| **X-XSS-Protection** | Protects against Cross-Site Scripting (XSS) attacks |
| **Referrer-Policy** | Controls referrer information sent with requests |

---

## 📌 Project Structure

```
web_scanner/
├── scripts/                # Python scripts
│   ├── security_scanner.py # Web security scanner script
├── logs/                   # Stores scan results
│   ├── security_scan_results.txt
├── docs/                   # Documentation
├── urls.txt                # Websites to scan
├── README.md               # Project documentation
├── .gitignore              # Ignored files
├── requirements.txt        # Python dependencies
└── venv/                   # Virtual environment
```

---

## 💡 Future Enhancements

✅ Add JSON & CSV output for reporting  
✅ Implement multi-threaded scanning for speed  
✅ Scan for missing `Permissions-Policy` and `Expect-CT` headers  
✅ Automate GitHub Actions for regular scans  

---

## 🤝 Contributing

Want to improve this tool? Feel free to fork the repo, create an issue, or submit a pull request.

---

## 🔗 Useful References

- 🔹 [OWASP Secure Headers](https://owasp.org/www-project-secure-headers/)
- 🔹 [Mozilla HTTP Security Guidelines](https://infosec.mozilla.org/guidelines/web_security)
- 🔹 [Google Web Security Best Practices](https://web.dev/security-headers/)

---

## 🐝 License

This project is licensed under the **MIT License**. See the `LICENSE` file for more details.

---



