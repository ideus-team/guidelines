#OS settings

## 1. Install Git
### 1.1 Install [msysgit](http://msysgit.github.io/):
 - Next → Next
 - Ajusting your PATH environtment — select „Run from the Windows command prompt“
 - Configuring the line endings conversions — select „Checkout as-is, commit as-is“
 - and Next → Next and so on.


### 1.2 Install [TortoiseGit](https://code.google.com/p/tortoisegit/wiki/Download)
x64 version.
Start → Tortoise Git → Settings:
  - TortoiseGit → Settings → Git → Credential
  - - Credential helper → Select „wincred“

## 2. GitHub
Регистрируемся на [GitHub](https://github.com/) если не зарегены. Стучимся в https://github.com/ideus-team


## 3. Ставим Photoshop с плагинами
 - Photoshop CC x64 v15
 - CSS Hat 2
 - PNG Hat


## 4. Настройки
###Исключения SVN/Git
 * dev/.sass-cache
 * dev/node_modules
 * css/main.css
 * js/scripts.js

###Исключения Total Commander
 * .sass-cache
 * node_modules
 * Thumbs.db
 * desktop.ini
 * .svn
 * .git

Причины:
 1. При коммите они будет попадать в SVN/Git, а это не имеет смысла для служебных файлов (мусор).
 2. Для генерируемых файл хранение в SVN/Git создаёт конфликты merge.
 3. При синхронизации с FTP они будет попадать на сайт, а это не имеет смысла (мусор).
 4. Служебные файлы SVN и GIT при появлении на FTP являются дырой в безопасности т.к. они содержат исходники сайта.
