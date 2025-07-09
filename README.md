<h1 align="center">🔒 chgpass</h1>

<p align="center">
  تغییر سریع پسورد کاربر به مقدار دلخواه یا رمز تصادفی
  <br>
  Change user password quickly via CLI (manual or random)
  <br>
  Changer le mot de passe utilisateur facilement (manuel ou aléatoire)
</p>

---

## 📦 ویژگی‌ها | Features | Fonctionnalités

- ✅ تغییر پسورد کاربر فعلی (SUDO_USER یا خودکار)
- 🔐 تولید رمز عبور تصادفی ایمن (base64 یا urandom)
- ⚡ اجرا با یک دستور ساده در ترمینال
- 🌐 چندزبانه و قابل نصب در `PATH`
- 📜 بدون ذخیره رمز عبور؛ فقط نمایش در خروجی

---

## 🛠 نصب | Installation | Installation

```bash
git clone https://github.com/rzadrbi/chgpass.git
sudo cp chgpass/bin/chgpass /usr/local/bin/
sudo chmod 700 /usr/local/bin/chgpass
