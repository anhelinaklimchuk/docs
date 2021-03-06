###Віджет для плагіна ManagerManager, дозволяє в зручній формі додавати теги до документів (для потрібної TV автоматично формується «список» вибору з усіма тегами, при цьому, нові теги просто вписуються через роздільник тут же) на сторінці редагування документа.

*TV повинна бути текстового типу.*

mm_widget_tags($fields, $delimiter, $source, $display_count, $roles, $templates);

####Опис параметрів
Назва|Опис|Допустимі значення|Значення за замовчуванням|Обов'язковий?
--------|--------|---------|--------|--------
fields|TV, для яких необхідно відобразити теги.|{comma separated string}|—|true
delimiter|Роздільник між тегами в полі|{string}|','|false
source|TV, з яких повинні братися теги для списку вибору. Це дозволяє використовувати різні поля для введення тегів і формування списку вибору. За замовчуванням значення береться з параметра «fields». Не використовуйте цей параметр, якщо не впевнені.|{comma separated string}|fields|false
display_count|Чи відображати в списку вибору кількість документів, в яких використовується тег (в скобочках после самого тега)?|{boolean}|false|false
roles|Ролі, для яких необхідно застосувати віджет, порожнє значення — всі ролі.|{comma separated string}|—|false
templates|Id шаблонів, для яких необхідно застосувати віджет, порожнє значення — всі шаблони.|{comma separated string}|—|false

####Приклади
Зробити для TV «docTags» віджет тегів у всіх документів (де вона використовуєте) для всіх ролей
	
	mm_widget_tags('docTags');
Зробити для TV «docTags» і «blogTags» віджет тегів у всіх документів (де вони використовуються) для всіх ролей.
При цьому, списки вибору тегів і кількість документів, які використовують кожен тег будуть однаковими для обох TV.
	
	mm_widget_tags('docTags,blogTags');
Зробити для TV «docTags» віджет тегів з відображенням кількості документів, що використовують кожен тег поруч з ним у документів з id шаблону = 2 для всіх ролей
	
	mm_widget_tags('docTags', ',', '', '1', '', '2');
