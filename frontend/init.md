#Установка окружения под Windows
##SASS, Compass, Grunt, Git и т.д.

##### 1. Ставим [Node.js](http://nodejs.org/download/)
Версия x64, нужен для Grunt.

##### 2. Ставим [Ruby](http://rubyinstaller.org/downloads/)
Версия x64, отмечаем Add Ruby executables to your PATH, нужен для SASS.

##### 3. Ставим SASS и Compass
```
gem install sass
gem install compass
```

##### 4. Ставим Grunt
```
npm install grunt-cli -g
```

##### 5. Ставим Git
###### 5.1 Ставим [msysgit](http://msysgit.github.io/):
 - Далее→Далее
 - Ajusting your PATH environtment - выбрать "Run from the Windows command prompt"
 - и снова Далее→Далее.

###### 5.2 Ставим [TortoiseGit](https://code.google.com/p/tortoisegit/wiki/Download)
Версия x64.

##### 6. Настройка GitHub
Регистрируемся на [GitHub](https://github.com/) если не зарегены.
```
git config --global user.name "Ваше имя на GitHub"
git config --global user.email "ваш_email@на GitHub"
```
Генерируем ключи:
```
"c:\Program Files (x86)\Git\bin\ssh-keygen.exe" -t rsa -C "ваш_email@на GitHub"
```
 - Enter file in which to save the key (//.ssh/id_rsa) - напишите что-то вроде "ваше-имя-на-github"
 - Enter passphrase (empty for no passphrase) - ничего не вводите, просто Enter

После этого Вы получите два файла с ключами в папке %userprofile%
[На GitHub в поле SSH Public Key](https://github.com/settings/ssh) вставляем содержимое файла ваше-имя-на-github.pub, или как вы его там назвали при создании ключей. Поле Title оставляете пустым, заполняете только Key.

##### 7. Делаем чекаут нашего HTML Framework
 - Создаём папку html-framework
 - Правой кнопкой - Git Clone
 - URL: https://github.com/ideus-team/html-framework.git
 - Load Putty Key

##### 8. Всё готово!
Уже настроенный для работы фреймворк лежит у нас на Github: https://github.com/ideus-team/html-framework.

Для начала работы с каждым из проектов необходимо запустить файл `install.bat` в директории `dev` - он запускает Grunt вместе с SASS, Compass и всем необходимым, а также проверяет необходимость их обновления.
Также следует добавить в исключения для системы контроля версий следующие пути:
 - `dev/node_modules`
 - `dev/.sass-cache`
 - `css/main.css`
 - `js/scripts.js`
