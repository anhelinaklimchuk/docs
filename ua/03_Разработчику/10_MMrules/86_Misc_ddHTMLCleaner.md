###Віджет для плагіна ManagerManager. Очищає зайві атрибути і стилі в HTML для необхідних полів документа (і TV).

####Опис параметрів
Назва|Опис|Допустимі значення|Значення за замовчуванням|Обов'язковий?
--------|--------|---------|--------|--------
fields|Поля документа (або TV), для яких необхідно застосувати віджет.|{comma separated string}|—|true
roles|Ролі, для яких необхідно застосувати віджет, порожнє значення — всі ролі.|{comma separated string}|—|false
templates|Id шаблонів, для яких необхідно застосувати віджет, порожнє значення — всі шаблони.|{comma separated string}|—|false
validAttrsForAllTags|Дозволені атрибути для всіх тегів (атрибути, які не потрібно видаляти, інші видаляться).|{comma separated string}|'title,class'|false
validStyles|Дозволені стилі для всіх тегів (стилі, які не потрібно видаляти з атрибута «style»).|{comma separated string}|'word-spacing'|false
validAttrs|Дозволені атрибути для тегів (вони не будуть видалятися). В якості ключа використовується і'мя тега, в якості значення — дозволені атрибути (рядок, розділена через кому).|{string: JSON}|'{"img":"src,alt,width,height","a":"href,target"}'|false
