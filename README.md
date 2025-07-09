# 🔒 chgpass

A simple CLI tool to change a user’s password to a specified value or a securely generated random string.  
<p dir="rtl">ابزاری خط فرمان ساده برای تغییر رمز عبور کاربر به مقدار دلخواه یا تولید خودکار یک رمز تصادفی امن</p>  
Un outil CLI simple pour modifier le mot de passe d’un utilisateur en une valeur définie ou aléatoire.

---

## 🇬🇧 English

### Introduction  
chgpass is a lightweight Bash script that allows you to change the password for any Linux user quickly—either to a provided password or to a random, secure 16-character string. The script detects the target user (invoking user via SUDO_USER) and executes safely with root privileges.

### Features  
- Change the target user’s password to a user-supplied value  
- Auto-generate a 16-character random password with `openssl` or fallback to `/dev/urandom`  
- No external dependencies beyond standard Linux utilities  
- Single-command usage: `sudo chgpass [NEW_PASSWORD]`  
- Passwords are never stored on disk, only printed to stdout  
- Easy installation: drop into your `PATH` as an executable  

### Installation  
```bash
git clone https://github.com/rzadrbi/chgpass.git
sudo cp chgpass/bin/chgpass /usr/local/bin/
sudo chmod 700 /usr/local/bin/chgpass
```
Ensure `/usr/local/bin` is in your `$PATH`:
```bash
echo $PATH
```

### Usage  
```bash
# 1) Set a custom password for the invoking user:
sudo chgpass MyCustom#Password

# 2) Generate and display a secure random password:
sudo chgpass
# Example Output:
# ✔ reza password changed to random value:
#   Ab3kL9xPq2Tz7YwR
```

### How It Works  
1. **Identify target user**: uses `$SUDO_USER` if run with `sudo`, else `whoami`.  
2. **Root check**: aborts if not executed as root (`EUID != 0`).  
3. **Password selection**:  
   - If `NEW_PASSWORD` argument is provided, uses it.  
   - Otherwise, generates a random 16-char password via `openssl rand -base64 12` or `tr -dc 'A-Za-z0-9._%+-' </dev/urandom | head -c16`.  
4. **Password change**: pipes `username:password` to `chpasswd` for secure update.  
5. **Output**: prints a confirmation message and, if random, displays the new password.

### Security Notes  
- Requires root privileges (via `sudo`).  
- Script installed with `chmod 700` ensures only root can read/execute.  
- Passwords are displayed only in your terminal session, never recorded to disk.  

### Contributing  
Issues, suggestions, and pull requests are welcome!  
```bash
# Fork → Clone → Edit → Commit → PR
```

### Contact  
- GitHub: https://github.com/rzadrbi/chgpass  
- Email: rzadrbi@gmail.com  

---

## 🇮🇷 فارسی

### معرفی  
<p dir="rtl">chgpass یک اسکریپت Bash سبک‌وزن است که امکان تغییر سریع رمز عبور کاربران لینوکس را فراهم می‌کند. می‌توانید رمز را به مقدار دلخواه تنظیم کنید یا یک رمز تصادفی ۱۶ کاراکتری امن تولید کنید.</p>

### قابلیت‌ها  
- <p dir="rtl">تغییر رمز کاربر هدف به رمز دلخواه</p>  
- <p dir="rtl">تولید خودکار رمز ۱۶ کاراکتری امن با `openssl` یا `/dev/urandom`</p>  
- <p dir="rtl">بدون نیاز به بسته‌های اضافی؛ فقط ابزارهای استاندارد</p>  
- <p dir="rtl">اجرای یک‌دستوری: `sudo chgpass [NEW_PASSWORD]`</p>  
- <p dir="rtl">عدم ذخیره رمز روی دیسک؛ فقط نمایش در ترمینال</p>  

### نصب  
```bash
git clone https://github.com/rzadrbi/chgpass.git
sudo cp chgpass/bin/chgpass /usr/local/bin/
sudo chmod 700 /usr/local/bin/chgpass
```
<p dir="rtl">مطمئن شوید `/usr/local/bin` در متغیر PATH شما قرار دارد:</p>
```bash
echo $PATH
```

### نحوه استفاده  
```bash
# ۱) تنظیم رمز دلخواه برای کاربر فعلی:
sudo chgpass MyCustom#Password

# ۲) تولید و نمایش رمز تصادفی امن:
sudo chgpass
# مثال خروجی:
# ✔ reza password changed to random value:
#   Ab3kL9xPq2Tz7YwR
```

### جزئیات اسکریپت  
<p dir="rtl">۱. شناسایی کاربر هدف: استفاده از `SUDO_USER` یا `whoami`.<br>
۲. بررسی سطح دسترسی: اجرا تنها با root (توقف در صورت عدم دسترسی).<br>
۳. انتخاب رمز:<br>
&nbsp;&nbsp;• اگر آرگومان رمز وجود داشته باشد، از آن استفاده می‌شود.<br>
&nbsp;&nbsp;• در غیر این صورت، رمز تصادفی ۱۶ کاراکتری تولید می‌شود.<br>
۴. تغییر رمز: ارسال `username:password` به `chpasswd`.<br>
۵. نمایش: پیام موفقیت و نمایش رمز در صورت رندوم بودن.</p>

### نکات امنیتی  
- <p dir="rtl">لزوم اجرای اسکریپت با `sudo` (دسترسی root).</p>  
- <p dir="rtl">مجوز فایل 700: فقط root می‌تواند اجرا یا خواند.</p>  
- <p dir="rtl">رمزها تنها در خروجی نمایش داده می‌شوند، ذخیره نمی‌شوند.</p>  

```bash
# Fork → Clone → Edit → Commit → PR
```

### تماس  
- GitHub: https://github.com/rzadrbi/chgpass  
- ایمیل: rzadrbi@gmail.com  

---

## 🇫🇷 Français

### Introduction  
chgpass est un script Bash léger permettant de modifier rapidement le mot de passe d’un utilisateur Linux soit avec une valeur fournie, soit avec une chaîne aléatoire sécurisée de 16 caractères.

### Fonctionnalités  
- Modifier le mot de passe de l’utilisateur cible vers une valeur spécifiée  
- Générer un mot de passe aléatoire de 16 caractères via `openssl` ou `/dev/urandom`  
- Aucune dépendance externe (utilitaires Linux standard)  
- Utilisation en une seule commande : `sudo chgpass [NEW_PASSWORD]`  
- Les mots de passe ne sont pas enregistrés sur le disque, uniquement affichés en stdout  

### Installation  
```bash
git clone https://github.com/rzadrbi/chgpass.git
sudo cp chgpass/bin/chgpass /usr/local/bin/
sudo chmod 700 /usr/local/bin/chgpass
```
Assurez-vous que `/usr/local/bin` est dans votre `$PATH` :
```bash
echo $PATH
```

### Utilisation  
```bash
# 1) Définir un mot de passe personnalisé :
sudo chgpass MotDePasse#Perso2025

# 2) Générer et afficher un mot de passe aléatoire :
sudo chgpass
# Exemple de sortie :
# ✔ reza password changed to random value:
#   Ab3kL9xPq2Tz7YwR
```

### Détails du script  
1. **Identification de l’utilisateur cible** : utilise `$SUDO_USER` ou `whoami`.  
2. **Vérification root** : nécessité d’être exécuté en root (`EUID == 0`).  
3. **Sélection du mot de passe** :  
   - si `NEW_PASSWORD` est passé en argument, l’utilise.  
   - sinon génère un mot de passe aléatoire de 16 caractères.  
4. **Changement du mot de passe** : transmet `username:password` à `chpasswd`.  
5. **Affichage** : message de succès et affichage du nouveau mot de passe si généré aléatoirement.

### Sécurité  
- Exécution requise en root (`sudo`).  
- Permissions du script définies à 700 (root only).  
- Les mots de passe ne sont jamais stockés sur le disque.

### Contribuer  
Issues, PR et suggestions sont les bienvenus !

### Contact  
- GitHub : https://github.com/rzadrbi/chgpass  
- Email : rzadrbi@gmail.com
