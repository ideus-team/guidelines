#How to install and run HTML Framework
Our HTML Framework based on H5BP+Grunt+SASS.

Instalation procedure is similar for Win/Mac/Linux.

## 1. Install [Node.js](http://nodejs.org/download/)
Windows Installer 64-bit (needed for Grunt).


## 2. Install [Ruby](http://rubyinstaller.org/downloads/)
Ruby __2.2.X__ x64 installer (needed for SASS (grunt-contrib-sass).  
 - Select __„Add Ruby executables to your PATH“__.


## 3. Install SASS+Bourbon
```
gem install sass
gem install bourbon
gem install neat
gem install bitters
```
3.1 Install Compass for old projects (only if you work at iDeus!):
```
gem install compass
```
If you get SSL error — foolow [this steps](https://gist.github.com/luislavena/f064211759ee0f806c88#manual-solution-to-ssl-issue).


## 4. Install Grunt
```
npm install grunt-cli -g
```

## 5. Get Framework
Git Clone:
 - URL: https://github.com/ideus-team/html-framework.git


## 6. Install Framework
Once run `dev/install.ps1`
Start Grunt with `dev/start.ps1`
