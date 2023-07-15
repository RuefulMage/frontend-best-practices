# Общее

- [1](#1) Отступы делать пробелами, на проекте во всех файлах html, css, etc должен быть одинаковый отступ — либо 4, либо 2 пробела. Нужно, чтобы не было проблем с отображением на разных ОС, редакторах и т.д.
- [2](#2) Проверять верстку при разных размерах экрана.
- [3](#3) Комментарий к коммиту формировать следующим образом:
  - Если это задача, то `DEV-[название задачи] [комментарий коммита с маленькой буквы]`.
    
    Пример: `DEV-123 added some changes`.
  - Если хот-фикс(срочное, небольшое исправление какого-то критического бага), то `HOT-FIX [комментарий коммита с маленькой буквы]`.

    Пример: `HOT-FIX fixed bug with multiplayer`.
- [4](#4) Ветки именовать следующим образом:
  - Если это задача, то `DEV-[название задачи]/[краткое описание ветки с маленькой буквы и слова разделены дефисом]`.

    Пример: `DEV-123/multiplayer-refactoring`.
  - Если хот-фикс(срочное, небольшое исправление какого-то критического бага), то `HOT-FIX/[краткое описание ветки с маленькой буквы и слова разделены дефисом]`.

    Пример: `HOT-FIX/multiplayer-bugs`.
- [5](#5) Коммиты должны содержать атомарные изменения, не нужно все изменения сливать в один коммит.
- [6](#6) Не нужно использовать `push --force` по отношению к мастеру, только в крайних случаях. Если нужно откатить коммит, лучше использовать `git revert`.
- [7](#7) В верстке используем [БЭМ](https://yandex.ru/dev/bem/), но с двумя отличиями:
  - В отличие от оригинального БЭМ не нужно писать в названиях классов имя блока, можно только элемент и модификатор 
    Например вместо `header__link` можно просто `link`. У нас Ангуляр, который инкапсулирует стили внутри компонента.
  - Не использовать миксины. Для позиционирования использовать компонент-обертку, а для кастомизации пропсы и модификаторы.