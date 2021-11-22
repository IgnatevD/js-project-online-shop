# Доска объявлений

## Исходные данные

### [Макет](https://www.figma.com/file/PGo6sP5hU9GlBBZzI1i608/OLX?node-id=2854%3A202), [API](https://callboard-backend.goit.global/api-docs)

## Адресная строка

| Ссылка | Значение | Шаблоны |
| ------ | -------- | :-----: |
| / | Главная страница:<br/>Реклама, Распродажа, категории. | **categories.hbs** со вложенным **card.hbs** |
| /index.html | Заменить на `/`, чтобы глаза не мозолило. | --//-- |
| /?categories=`имя`,`имя` <sup>*</sup> | Фильтрация категорий на главной странице. | --//-- |
| /profile <sup>**</sup> | Личная страница пользователя:<br/>Мои объявления и Избранное. | --//-- |
| /category/`имяКатегории` | Подробное отображение отдельной категории. | **search-allcard.hbs** со вложенным **category-cards.hbs** |
| /?search=`запрос` | Поиск товаров. | --//-- |
| /profile/own <sup>**</sup> | Мои объявления. | --//-- |
| /profile/favourite <sup>**</sup> | Избранное. | --//-- |
| /login | Модальное окно регистрации,<br/>по закрытию рисует страницу `/profile` | Страница не перерисовывается |
| /login?redirect=`ссылка` | Модальное окно регистрации,<br/>по закрытию рисует то, что по `ссылке` | --//-- |
| \#`id товара` | Модальное окно с подробными сведениями о товаре | --//-- |

<sup>*</sup> - фактически в адресной строке вместо запятой мы увидим `%2С`.
<sup>**</sup> - если пользователь не залогинен, формируется редирект.