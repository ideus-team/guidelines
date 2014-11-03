This document outlines the way @iDeus_team is expected to write their HTML markup. Following this document ensures that everyone is writing markup is doing so with good practices and accessibility in mind.
This document borrows ideas from:

 * https://github.com/mobify/mobify-code-style/tree/master/html
 * [Google's HTML Style Guide](https://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml)
 * [SMACSS](http://smacss.com/book/formatting)
 * [CSSComb](http://csscomb.com)
 * [BEM](http://bem.info)

Мы намеренно сокращаем правила для удобочитаемости и не пишем в стиле КО a-la "Separate structure from presentation from behavior" и "Items in list form should always be in <ul>, <ol>, or <dl>. Never use a set of <div> or <p>".
Также мы не описываем очевидные правила, которые могут быть проверены автоматически во время сборки, типа "Use valid HTML where possible", "Avoid specifying units for zero values", и правила форматирования (типа "Include one space before the opening brace of declaration blocks. Include one space after ":" in each property. Use a semicolon after every declaration. Include one space befor every new declaration.") что понятны из примера кода.


##HTML:
###1. Formatting Rules:
 - 2 space indent
 - lowercase
 - double quotes
 - new line for everything
 - use Common Internet Scheme Syntax (i.e. omit the protocol from embedded resources).
 
###2. Naming
Мы используем BEM. Наши BEM-гайдлайны будут расписаны в отдельном документе.

####Страницы
маленькие-буквы-через-тире.html
Название должно быть на английском (а не translitom), отражать смысл страницы и красиво выглядеть. Думайте головой чтоб не создавать страницы типа econom_final_30.html или aurora_landing.html

####Картинки
Называются согласно имени блока. Рекомендуется добавлять суффиксы: -bg, -btn и т.д., а для временных заглушек префикс temp-. Например: b-socialLinks-ico.png
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

```
<div class="b-someBlock b-text -style_notice -state_modal">
  <p>
    Some text.
    <img class="b-someBlock__cover" src="//site-name.com/img/b-someBlock__cover-ill.jpg" alt="some description" />
  </p>
</div>
```

##CSS:
1. Multiple lines, groped by CSSComb declaration order
2. Single quotes
3. CSSDoc for comment blocks.
```
/**
* @section Some Block
*/
.b-someBlock {
  position: absolute;
  z-index: 10;
  top: 10px; 
  right: 10px; 
  bottom: 10px; 
  left: 10px;
  
  display: none;
  overflow: hidden;
  

  width: 100px; 
  height: 200px;
  margin: 10px; 
  padding: 20px 30px;
  
  opacity: .5;
  bacground-color: #f00;
  background-image: 
    linear-gradient(to bottom right, #f00, rgba(0,0,0,.1)),
    url('../img/b-someBlock.png');
  background-size: cover;
}
```

Single line versus multiple lines - please read Jonathan Snook http://smacss.com/book/formatting

Be consistent.
