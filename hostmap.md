## Организация файлов и папок на основном сервере
> [greenproject.me](//greenproject.me)

На основном сервере находится сайт компании, а также продукты, проекты и заказы, зачастую на дочерних доменах.

#### Список дочерних доменов
> [beta.greenproject.me](//beta.greenproject.me) - dev-ветка сайта компании  
> [game.greenproject.me](//game.greenproject.me) - разработка игры  
> [brand.greenproject.me](//brand.greenproject.me) - brandbook и информация по дизайну  
> [order.greenproject.me](//order.greenproject.me) - текущие заказы компании  
> [project.greenproject.me](//project.greenproject.me) - проекты компании  
> [portfolio.greenproject.me](//portfolio.greenproject.me) - архив работ
>
> продукты  
> [blog.greenproject.me](//beta.greenproject.me) - пример блог-сайта  
> [page.greenproject.me](//beta.greenproject.me) - пример лендинга  
> [store.greenproject.me](//beta.greenproject.me) - пример сайта-магазина  
> [promo.greenproject.me](//beta.greenproject.me) - пример промо-сайта  
> [forum.greenproject.me](//beta.greenproject.me) - пример форума
>
> сервисы  
> [service.greenproject.me](//service.greenproject.me) - продукты для помощи при разработке

#### ВНИМАНИЕ!
> На дочерних доменах недоступен протокол __https://__

В большинстве дочерних доменов наведены `soft-link` ссылки на основные папки репозиториев, используемых при разработке

#### Организация файлов
```
public_html/    - root catalog folder
  less.js
  api/          - greenprojectme/api repository
    index.html  - readme (web-версия)
  xjsl/
    index.html  - readme (web-версия)

  *.html        - страницы сайта
  media/        - медиаобъекты
    image/      - медиаобъекты / изображения
    audio/      - медиаобъекты / аудиофайлы
    video/      - медиаобъекты / видеофайлы
    font/       - медиаобъекты / шрифты
    style/      - стили сайта   (css, less)
    script/     - скрипты сайта (js)
  server/
    *.php       - серверная логика
  include/
  content/      - содержимое сайта

  beta/         - beta.greenproject.me
    -s api/
    -s xjsl/
    -s less.js
  game/         - game.greenproject.me
    -s api/
    -s xjsl/
    -s less.js
  brand/        - brand.greenproject.me
    -s api/
    -s xjsl/
    -s less.js
    favicon.png - иконка сайта
    style/      - корпоративный стиль
  order/        - order.greenproject.me
    -s api/
    -s xjsl/
    -s less.js
  project/      - project.greenproject.me
    -s api/
    -s xjsl/
    -s less.js
  portfolio/    - portfolio.greenproject.me
    -s api/
    -s xjsl/
    -s less.js

  blog/         - blog.greenproject.me
    -s api/
    -s xjsl/
    -s less.js
  page/         - page.greenproject.me
    -s api/
    -s xjsl/
    -s less.js
  store/        - store.greenproject.me
    -s api/
    -s xjsl/
    -s less.js
  promo/        - promo.greenproject.me
    -s api/
    -s xjsl/
    -s less.js
  forum/        - forum.greenproject.me
    -s api/
    -s xjsl/
    -s less.js

  service/      - service.greenproject.me
    -s api/
    -s xjsl/
    -s less.js
    less/      - компилятор less
    page/      - конструктор page-проектов
```

При создании новой папки для дочернего домена лучше использовать скрипт `../folder.sh` для автоматического наведения ссылок
```sh
$ sh ../folder.sh %foldername%

// Результат
$ ls %foldername%
api/
xjsl/
brand/
less.js
```
