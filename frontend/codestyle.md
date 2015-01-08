This document outlines the way @iDeus_team is expected to write their HTML markup. Following this document ensures that everyone is writing markup is doing so with good practices and accessibility in mind.
This document borrows ideas from:
 * [Google's HTML Style Guide](https://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml)
 * [SMACSS](http://smacss.com/book/formatting)
 * [CSS Guidelines by Harry Roberts](http://cssguidelin.es/)

Мы намеренно сокращаем правила для удобочитаемости и не пишем в стиле КО a-la "Separate structure from presentation from behavior" и "Items in list form should always be in `<ul>`, `<ol>`, or `<dl>`".
Также мы не описываем очевидные правила, которые могут быть проверены автоматически во время сборки, типа "Avoid specifying units for zero values", и правила форматирования (типа "Include one space before the opening brace of declaration blocks…") что понятны из примера кода.

##HTML
```
<div class="b-someBlock b-text -style_notice -state_modal">
  <p>
    Some text.
    <img class="b-someBlock__cover" src="//site-name.com/img/someBlock__cover-ill.jpg" alt="some description" />
  </p>
</div>
```
###1. Formatting Rules
1. [NO TABS, 2 space indent](https://github.com/ideus-team/guidelines/blob/master/frontend/tabs.md)
2. lowercase
3. Double quotes
4. New line for everything
5. Omit the protocol from embedded resources.
 
###2. Naming
Мы используем [BEM CSS](https://github.com/ideus-team/guidelines/blob/master/frontend/bem.md).

####Страницы
маленькие-буквы-через-тире.html
Название должно быть на английском (а не translitom), отражать смысл страницы и красиво выглядеть. Думайте головой чтоб не создавать страницы типа econom_landing_30.html.

####Картинки
Называются согласно имени блока без префикса. Рекомендуется добавлять суффиксы: -bg, -btn и т.д., а для временных заглушек префикс temp-. Например: socialLinks-ico.png
Суффикс в конце, чтоб легче было выделять блоки картинок и копировать на другие проекты.
 * bg    : background т.е. для фоновых изображений и фонов
 * btn   : button, кнопки
 * ill   : illustartion - для картинок-иллюстраций
 * photo : для фотографий
 * bull  : bullets - для "буллетов", пиктограмм элементов списка
 * logo  : для логотипов
 * ico   : icons - для иконок
 * text  : для текстовых надписей, сохранённых как картинки
 
####Тестовые ресурсы
Тестовые файлы должны иметь префикс test-номерТикета-.
Например test-2567-script.js

##CSS
```
/**
* @section Some Block
*/
.b-someBlock {
  margin: 10px; 
  padding: 20px 30px;
  width: 100px; 
  height: 200px;  
  
  opacity: .5;
  bacground-color: #f00;
  background-image: 
    linear-gradient(to bottom right, #f00, rgba(0,0,0,.1)),
    url('../img/someBlock.png');
  background-size: cover;
}
```
1. [NO TABS](https://github.com/ideus-team/guidelines/blob/master/frontend/tabs.md)
2. [Multiple lines](http://smacss.com/book/formatting), groped by [CSSComb](http://csscomb.com) with  [zen-coding](https://github.com/csscomb/csscomb.js/blob/master/config/zen.json) declaration order
3. Single quotes
4. [CSSDoc](http://habrahabr.ru/post/87406/) for comment blocks.

##JS
```
/**
 * This is a description of the someFunction function
 * @function someFunction
 * @requires momentjs {@link https://github.com/moment/moment/}
*/
function someFunction() {
  return 1;
}
```
1. NO TABS, 2 space indent
2. camelCase
3. [JSDoc](http://usejsdoc.org/) for comment blocks.

PS.
Be consistent.
