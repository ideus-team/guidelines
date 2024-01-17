# OS settings

## 1. Install Git
### 1.1 Install [Git for Windows](https://git-scm.com/downloads/):
 - Next → Next
 - **Ajusting your PATH environtment** — select "Use Git from the Windows command prompt"
 - **Configuring the line endings conversions** — select "Checkout as-is, commit as-is"
 - and Next → Next and so on.


### 1.2 Install [TortoiseGit](https://code.google.com/p/tortoisegit/wiki/Download)
x64 version. Next → Next → Done.
Start → Tortoise Git → Settings:
 - **Git** — Set "Name" & Email" for **Global** config source

## 2. GitHub
Реєструємося на [GitHub](https://github.com/), якщо ще не зареєстровані. Стукаємо до https://github.com/ideus-team

## 3. Встановлюємо софт з [HTML-framework](https://github.com/ideus-team/html-framework)
Кроки 1-5

## 4. Налаштування
### Винятки SVN/Git
```
dev/.sass-cache
dev/node_modules
css/main.css
js/scripts.js
```

### Винятки Total Commander / WinSCP / etc.
```
.svn
.git
.sass-cache
node_modules
Thumbs.db
desktop.ini
```

Причини:
  1. При комміті вони потраплятимуть у SVN/Git, але це немає сенсу для службових файлів (сміття).
  2. Для генерованих файл зберігання SVN/Git створює конфлікти merge.
  3. При синхронізації з FTP вони потраплятимуть на сайт, а це не має сенсу (сміття).
  4. Службові файли SVN і GIT з появою на FTP є дірою у безпеці бо вони містять вихідники сайту.
