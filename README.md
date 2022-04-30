## Занятие #48. Лабораторная работа
Напишите прототип электронного магазина.
Общие указания
Страницы должны быть стилизованы вручную или с помощью Bootstrap.
Проект должен находиться под версионным контролем и в репозитории должно быть не меньше 5 осмысленных коммитов.
# Этап 1
Инициализируйте проект и создайте модель "Товар" (Product), содержащую поля:
Наименование товара - строка до 100 символов, обязательное
Описание товара - текст до 2000 символов, необязательное
Категория - текстовое поле с вариантами выбора (3-5 любых вариантов), обязательное, по умолчанию имеет значение "other" - "Разное".
Остаток - целочисленное поле, не может быть меньше 0.
Стоимость - десятичное, до 7 знаков, 2 знака после точки.

# Указания:
Зарегистрируйте модель в админ-панели.
Создайте суперадмина.
Добавьте 5-7 товаров для примера с разными данными
Создайте фикстуру с тестовыми данными.
Код категории должен быть записан в том же формате, что и имя переменной - на латинице, без пробелов. Название категории - в человеко-читаемом формате, для вывода на страницах сайта.
Не забудьте закоммитить миграцию!
# Этап 2
Создайте страницы просмотра товара:
Список товаров (главная страница).
Просмотр одного товара по id.

# Указания:
Добавьте базовый шаблон и меню навигации. В меню должна быть ссылка на главную страницу.
Для товаров на главной выводите их название, цену и категорию.
Для товаров на главной странице выводите ссылку на их просмотр. Можно сделать ссылкой название товара или вывести отдельную ссылку.
На странице детального просмотра товара выведите все его данные.
Для категорий выводите их названия, а не коды.
Не выводите на главной товары, остаток которых меньше 1 единицы.
Отсортируйте товары на главной по категориям и названиям в алфавитном порядке.

# Бонус:
Добавьте поиск товара по названию. Выведите на главной перед списком товаров форму, которая отправляется методом GET и фильтруйте товары по данным из запроса. Для формы должен быть создан класс формы с одним полем. (+0.2 балла).
# Этап 3.
Создайте страницы для изменения товара:
Добавление товара
Редактирование товара
Удаление товара

# Указания:
Удаление сделайте с подтверждением.
Для добавления и редактирования используйте общий шаблон формы.
Для остатка в форме используйте поле типа IntegerField. Используйте его свойство min_value, чтобы ограничить остаток товара не меньше 0.
Для цены используйте поле типа DecimalField с такими же настройками, как и в модели.
Добавьте ссылки на новые страницы на главную и на страницу просмотра товара.
Этап 4 (бонус, +0.3 балла)
Добавьте страницу для просмотра товаров по категориям.

# Указания:
Добавьте в меню или на главную страницу список категорий. Каждая категория в списке является ссылкой на страницу списка товаров в этой категории.
Код категории должен передаваться, как переменная url, например: /products/notebooks/ или /products/apples/ и т.д.
Страница просмотра товаров по категории должна выглядеть так же, как и главная страница, но на ней выводятся только товары в выбранной категории и в заголовке должно быть написано название категории.
Сортируйте товары в списке по названию в алфавитном порядке.
Используйте частичный шаблон для вывода списка товаров здесь и на главной странице.
Названия категорий на других страницах сделайте ссылками на эту страницу.
Здесь так же можно сделать поиск, как и на главной странице.

