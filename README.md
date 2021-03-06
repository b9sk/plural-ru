# plural-ru


Склонение русских существительных и глаголов!

### Установка

```
npm install --save plural-ru
```


Примеры:

```js
const plural = require('plural-ru');

// склонение существительного
plural(1, 'файл', 'файла', 'файлов'); // файл
plural(2, 'файл', 'файла', 'файлов'); // файла
plural(5, 'файл', 'файла', 'файлов'); // файлов

// склонение существительного + плейсхолдер
plural(1, '%d файл', '%d файла', '%d файлов'); // 1 файл
plural(2, '%d файл', '%d файла', '%d файлов'); // 2 файла
plural(5, '%d файл', '%d файла', '%d файлов'); // 5 файлов

// единственное и множественное число (если переданы 2 склонения)
plural(1, 'Оформить товар', 'Оформить товары'); // Оформить товар
plural(21, 'Оформить товар', 'Оформить товары'); // Оформить товары

// склонение глаголов 💥
plural.verb(1, 'нашлась', 'нашлись', 'нашлось'); // нашлась
plural.verb(2, 'нашлась', 'нашлись', 'нашлось'); // нашлись
plural.verb(5, 'нашлась', 'нашлись', 'нашлось'); // нашлось
```

Сложный пример из жизни:

```js
const found = plural.verb(
    foundCount,
    'нашлась',
    'нашлись',
    'нашлось'
);
const ideas = plural(
    foundCount,
    'идея',
    'идеи',
    'идей'
);

console.log(`${found} ${foundCount} ${ideas} ${forSite}`);
// нашлось 1000000 идей для вашего сайта!
```


