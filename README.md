# 🔒 chgpass

A simple CLI tool to change a user’s password to a specified value or to a securely generated random string.  


---

### 🚀 Features

- Change the target user’s password to a provided value  
- Generate a secure 16-character random password (via `openssl` or `/dev/urandom`)  
- Single–command usage: `sudo chgpass [NEW_PASSWORD]`  
- No password stored on disk—only printed to stdout  
- Installs into your `PATH` as a standalone executable  

### 🛠 Installation

```bash
git clone https://github.com/rzadrbi/chgpass.git
sudo cp chgpass/bin/chgpass /usr/local/bin/
sudo chmod 700 /usr/local/bin/chgpass
```

Ensure /usr/local/bin is in your PATH :
```echo $PATH```

💡 Usage
# 1) Set a custom password
```
sudo chgpass MySecret#123
```

# 2) Generate & display a random password
```
sudo chgpass

# ✔ reza password changed to random value:
#   Ab3kL9xPq2Tz7YwR
```


📁 Repository Structure
```
chgpass/
├── bin/
│   └── chgpass      ← the executable script
├── README.md        ← this document
└── LICENSE          ← MIT license
```
🔐 Security

📣 Contributing
Feel free to open issues, submit PRs or improvements!

