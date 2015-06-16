This document outlines the way @iDeus_team is expected to write their HTML markup. Following this document ensures that everyone is writing markup is doing so with good practices and accessibility in mind.
This document borrows ideas from:
 * [Google's HTML Style Guide](https://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml)
 * [SMACSS](http://smacss.com/book/formatting)
 * [CSS Guidelines by Harry Roberts](http://cssguidelin.es/)

Мы намеренно сокращаем правила для удобочитаемости и не пишем в стиле КО a-la "Separate structure from presentation from behavior" и "Items in list form should always be in `<ul>`, `<ol>`, or `<dl>`".
Также мы не описываем очевидные правила, которые могут быть проверены автоматически во время сборки, типа "Avoid specifying units for zero values", и правила форматирования (типа "Include one space before the opening brace of declaration blocks…") что понятны из примера кода.

##HTML
```html
<div class="b-someBlock b-text -style_notice -state_modal">
  <p>
    Some text.
    <img class="b-someBlock__cover js-someBlockCover" src="//site-name.com/img/someBlock__cover-ill.jpg" alt="some description" />
  </p>
</div>
```
###1. Formatting Rules
1. [NO TABS, 2 space indent](https://github.com/ideus-team/guidelines/blob/master/frontend/tabs.md)
2. lowercase
3. Double quotes
4. New line for everything
5. Omit the protocol from embedded resources.

###2. Naming Conversions
Мы используем [Соглашение об именовании](https://github.com/ideus-team/guidelines/blob/master/frontend/naming-conventions.md) блоков и файлов.


##CSS
```scss
/**
* @section Some Block
*/
.b-someBlock {
  $someBlock-color: #f00;

  margin: 10px;
  padding: 20px 30px;
  width: (100px - 30 * 2);
  height: (200px - 20px * 2);

  opacity: .5;
  background-color: $someBlock-color;
  background-image:
    linear-gradient(to bottom right, #f00, rgba(0,0,0,.1)),
    url('../img/blocks/someBlock/someBlock-bg.png');
  background-size: cover;

  %i-someBlock-mod_val {
    /* Some abstract block */
  }
  %i-someBlock__someElement {
    /* Some abstract element */
  }

  &__someElement {
    @extend %i-someBlock__someElement;
    transform: scale(.8);

    @media screen and (max-width: 800px) {
      transform: scale(.6);
    }
  }

  @at-root {
    @keyframes slidein {
      from {
        margin-left: 100%;
        width: 300%;
      }

      to {
        margin-left: 0%;
        width: 100%;
      }
    }
  }

  &:hover {
    animation: slidein .8s;
  }
}
}
```
###1. Formatting Rules
1. [NO TABS, 2 space indent](https://github.com/ideus-team/guidelines/blob/master/frontend/tabs.md)
2. [Multiple lines](http://smacss.com/book/formatting), groped by [CSSComb](http://csscomb.com) with  [zen-coding](https://github.com/csscomb/csscomb.js/blob/master/config/zen.json) declaration order
3. Single quotes
4. [CSSDoc](http://habrahabr.ru/post/87406/) for comment blocks.
5. Переменные нужно определять в пределах каждого блока (иначе когда копируешь блок в другой проект он остается с неопределёнными переменными).
6. Для значений, что зависят от других, необходимо использовать формулы и/или переменные.
7. Максимально используются возможности Sass, особенно в связке с BEM (`&__el`, `@extend %abstractBlock`).
8. Используется Автопрефиксер, поэтому префиксы у CSS писать не нужно.

###2. Naming Conversions
Мы используем [BEM CSS](https://github.com/ideus-team/guidelines/blob/master/frontend/bem.md)

##JS
```js
/**
 * This is a description of the someFunction function
 * @function someFunction
 * @requires momentjs {@link https://github.com/moment/moment/}
*/
function someFunction() {
  return 1;
}
```
###1. Formatting Rules
1. [NO TABS, 2 space indent](https://github.com/ideus-team/guidelines/blob/master/frontend/tabs.md)
2. [JSDoc](http://usejsdoc.org/) for comment blocks.

###2. Naming Conversions
We use camelCase.

P.S.
Be consistent.
