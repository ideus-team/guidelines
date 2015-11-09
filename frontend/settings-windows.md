#OS settings

## 1. Install Git
### 1.1 Install [msysgit](http://msysgit.github.io/):
 - Next → Next
 - __Ajusting your PATH environtment__ — select „Run from the Windows command prompt“
 - __Configuring the line endings conversions__ — select „Checkout as-is, commit as-is“
 - and Next → Next and so on.


### 1.2 Install [TortoiseGit](https://code.google.com/p/tortoisegit/wiki/Download)
x64 version. Next → Next → Done.
Start → Tortoise Git → Settings:
  - __TortoiseGit → Settings → Git → Credential → Credential helper__ — Select „wincred - current Windows user“

## 2. GitHub
Регистрируемся на [GitHub](https://github.com/) если не зарегены. Стучимся в https://github.com/ideus-team

## 3. Устанавливаем [софт для старых проектов](https://github.com/ideus-team/guidelines/blob/master/frontend/settings-old-projects.md):

## 4. Устанавливаем [HTML-framework](https://github.com/ideus-team/html-framework)

## 5. Ставим Photoshop с плагинами
 - Photoshop CC 2015 x64
 - CSS Hat 2
 - PNG Hat
 - [List Fonts](https://github.com/iamdarrenhall/list-fonts)

## 6. Настройки
###Исключения SVN/Git
```
dev/.sass-cache
dev/node_modules
css/main.css
js/scripts.js
```

###Исключения Total Commander
```
.svn
.git
.sass-cache
node_modules
Thumbs.db
desktop.ini
```

Причины:
 1. При коммите они будет попадать в SVN/Git, а это не имеет смысла для служебных файлов (мусор).
 2. Для генерируемых файл хранение в SVN/Git создаёт конфликты merge.
 3. При синхронизации с FTP они будет попадать на сайт, а это не имеет смысла (мусор).
 4. Служебные файлы SVN и GIT при появлении на FTP являются дырой в безопасности т.к. они содержат исходники сайта.
