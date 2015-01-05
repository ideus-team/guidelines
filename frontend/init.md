#Установка окружения под Windows
SASS, Compass, Grunt, Git и т.д.

## 1. Ставим [Node.js](http://nodejs.org/download/)
Версия x64, нужен для Grunt.


## 2. Ставим [Ruby](http://rubyinstaller.org/downloads/)
Версия x64, отмечаем Add Ruby executables to your PATH, нужен для SASS.


## 3. Ставим SASS и Compass
```
gem install sass
gem install compass
```


## 4. Ставим Grunt
```
npm install grunt-cli -g
```

## 5. Ставим Git
### 5.1 Ставим [msysgit](http://msysgit.github.io/):
 - Далее→Далее
 - Ajusting your PATH environtment - выбрать "Run from the Windows command prompt"
 - и снова Далее→Далее.


### 5.2 Ставим [TortoiseGit](https://code.google.com/p/tortoisegit/wiki/Download)
Версия x64.
Пуск→Tortoise Git→Settings: 
TortoiseGit→Settings→Git→Credential 
Credential helper→wincred


## 6. Настройка GitHub
Регистрируемся на [GitHub](https://github.com/) если не зарегены. Стучимся в https://github.com/ideus-team


## 7. [Настройки софта](https://github.com/ideus-team/guidelines/blob/master/frontend/settings.md)


## 8. Делаем чекаут нашего HTML Framework
 - Создаём папку html-framework
 - Правой кнопкой - Git Clone
 - URL: https://github.com/ideus-team/html-framework.git


## 9. Всё готово!
Для начала работы с каждым из проектов необходимо запустить файл `install.bat` в директории `dev` - он запускает Grunt вместе с SASS, Compass и всем необходимым, а также проверяет необходимость их обновления.
