###Віджет для плагіна ManagerManager, дозволяє приховувати поля документа або TV.

mm_hideFields(string $fields, string $roles, string $templates);


####Опис параметрів
Назва|Опис|Допустимі значення|Значення за замовчуванням|Обов'язковий?
--------|--------|---------|--------|--------
fields|Поля документа (або TV), які необхідно приховати.|{comma separated string}|—|true
roles|Ролі, для яких необхідно застосувати віджет, порожнє значення — всі ролі.|{comma separated string}|—|false
templates|Id шаблонів, для яких необхідно застосувати віджет, порожнє значення — всі шаблони.|{comma separated string}|—|false

####Приклади
Приховати поле «атрибуты ссылки» для всіх користувачів
	
	mm_hideFields('link_attributes');

Приховати поле «псевдоним» у документів з id шаблону = 3 для користувачів з id ролі = 1

	mm_hideFields('alias', '1', '3');

Приховати TV «myVar» для користувачів з id ролі = 2
	
	mm_hideFields('myVar', '2');
