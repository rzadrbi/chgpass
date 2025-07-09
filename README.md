# 🔒 chgpass

A simple CLI tool to change a user’s password to a specified value or a securely generated random string.  
ابزاری خط فرمان ساده برای تغییر رمز عبور کاربر به مقدار دلخواه یا رمز امن تصادفی  
Un outil en ligne de commande pour changer le mot de passe d’un utilisateur en une valeur définie ou aléatoire

---

## 🗂 Features | قابلیت‌ها | Fonctionnalités

- 🔐 Change user password to a specific value  
- 🎲 Generate secure 16-character random passwords (`openssl` or `/dev/urandom`)  
- ⚡ Fast one-line terminal usage: `sudo chgpass [PASSWORD]`  
- 🛡 No password stored—only printed to stdout  
- 📦 Easy installation into your PATH

---

## 🛠 Installation

```bash
git clone https://github.com/rzadrbi/chgpass.git
sudo cp chgpass/bin/chgpass /usr/local/bin/
sudo chmod 700 /usr/local/bin/chgpass
```

> Ensure `/usr/local/bin` is included in your `$PATH`.

---

## 🚀 Usage

```bash
# 1. Set custom password
sudo chgpass MySecurePassword2025

# 2. Auto-generate secure password
sudo chgpass
# ✔ reza password changed to random value:
#   Ab3kL9xPq2Tz7YwR
```

---

## 📁 Repository Structure

```
chgpass/
├── bin/
│   └── chgpass        # main executable script
├── README.md          # documentation file
└── LICENSE            # MIT license
```

---

## 🔐 Security Notes

- Root privileges required (via `sudo`)  
- File permissions locked to owner (`chmod 700`)  
- Passwords never saved—only output to terminal  

---

## 🌐 Multilingual Summary

<table>
<thead>
<tr>
<th>🇬🇧 English</th>
<th>🇮🇷 فارسی</th>
<th>🇫🇷 Français</th>
</tr>
</thead>
<tbody>
<tr>
<td>A minimal CLI tool to reset user passwords securely</td>
<td>ابزار خط فرمان سبک برای تغییر امن رمز عبور کاربران</td>
<td>Un outil minimal en ligne de commande pour réinitialiser les mots de passe utilisateur</td>
</tr>
<tr>
<td>Supports both manual and auto-generated passwords</td>
<td>پشتیبانی از رمز دلخواه و رمز تولید شده تصادفی</td>
<td>Supporte les mots de passe manuels ou générés automatiquement</td>
</tr>
</tbody>
</table>

---

## 📣 Contribute

Pull requests, bug reports and suggestions are always welcome!

```bash
# Fork → Clone → Edit → Commit → PR 🚀
```

---

## 📇 Contact

- GitHub: [rzadrbi](https://github.com/rzadrbi)  
- Email: [rzadrbi@gmail.com](mailto:rzadrbi@gmail.com)
