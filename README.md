# 🔒 chgpass

A simple CLI tool to change a user’s password to a specified value or to a securely generated random string.  
<p dir="rtl">ابزاری خط فرمان ساده برای تغییر پسورد کاربر به مقدار دلخواه یا تصادفی امن</p>  
Un outil en ligne de commande simple pour changer le mot de passe d’un utilisateur en une valeur choisie ou aléatoire.

---

## 🇬🇧 English

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
