#Установка окружения
SASS, Compass, Grunt, Git и т.д.
Почти всё одинаково для Win/Mac/Linux.

## 1. Ставим [Node.js](http://nodejs.org/download/)
Windows Installer 64-bit, нужен для Grunt.


## 2. Ставим [Ruby](http://rubyinstaller.org/downloads/)
Ruby _2.1.X_ x64 installer, отмечаем _"Add Ruby executables to your PATH"_, нужен для SASS (grunt-contrib-sass).


## 3. Ставим SASS+Compass,Bourbon&Co
1) Если выдает ошибку SSL сертификата — установите сертификат пройдя [эти шаги](https://gist.github.com/luislavena/f064211759ee0f806c88#manual-solution-to-ssl-issue).
```
gem install sass
gem install compass
gem install bourbon
gem install neat
gem install bitters
```


## 4. Ставим Grunt
```
npm install grunt-cli -g
```

## 5. Ставим Git
### 5.1 Ставим [msysgit](http://msysgit.github.io/):
 - Далее→Далее
 - Ajusting your PATH environtment — выбрать "Run from the Windows command prompt"
 - Configuring the line endings conversions — выбрать "Checkout as-is, commit as-is"
 - и снова Далее→Далее.


### 5.2 Ставим [TortoiseGit](https://code.google.com/p/tortoisegit/wiki/Download)
Версия x64.
Пуск→Tortoise Git→Settings:
TortoiseGit→Settings→Git→Credential
Credential helper→wincred


## 6. Настройка GitHub
Регистрируемся на [GitHub](https://github.com/) если не зарегены. Стучимся в https://github.com/ideus-team


## 7. Ставим Photoshop с плагинами
 - Photoshop CC x64 v15
 - CSS Hat 2
 - PNG Hat


## 8. [Настройки софта](https://github.com/ideus-team/guidelines/blob/master/frontend/settings.md)


## 9. Делаем чекаут нашего HTML Framework
 - Создаём папку html-framework
 - Правой кнопкой — Git Clone
 - URL: https://github.com/ideus-team/html-framework.git


## 10. Всё готово!
Для начала работы с каждым из проектов необходимо запустить файл `install.bat` в директории `dev` — он запускает Grunt вместе с SASS, Compass и всем необходимым, а также проверяет необходимость их обновления.
