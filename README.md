# 26.03.2021 OK это глобальное NGRAM обновление
Добавил файл N-GRAMS.xlsm

Он содержит  две функции (подобные той, про которую написано ниже), но работающие с помощью анализа NGRAM. Для поиска и сравнения строк длиной больше 1 слова это работает лучше Левенштейна (а может и для одного лучше).

Хэлп и описание находятся в самом файле. При желании сохраните N-GRAMS.xlsm как надстройку (.xlam) что бы эти формулы были всегда доступны.

# 26.03.2021 OK thats a major NGRAM upgrade
NGRAM code and formulas are in N-GRAMS.xlsm. Together with help and examples.

This is NGRAM text analysis on VBA in Excel. It is better for text more then 1 word long.

You can save as .xlam add-in and add reference to it for convenience.

----------------------------------------------

# VLOOKUPfuzzy
It's an Excel add-in with User Defined Function: =VLOOKUPfuzzy

This function is like regular VLOOKUP, but if it finds no exact match, it uses Levenshtein distance metric to find the closest (most similar) string.

VLOOKUPfuzzy could be userfull for normalising lists.

Use =VLOOKUPfuzzy_help() for help on parameters.


# ВПРнечеткий
Это надстройка Excel с пользовательской функцией: =ВПРнечеткий

Это функция работает как стандартная ВПР, но, если она не находит точное совпадение, то возващает наиболее "похожее" значение используя "Расстояние Левенштейна" как метрику сходства.

ВПРнечеткий может быть полезен при нормализации данных по справочникам.

Введите =ВПРнечеткий() для помощи по параметрам.


## Пример работы
ВНИМАНИЕ! Формула всегда выдает "какой-то" ответ, даже если с человеческой точки зрения он совсем не к месту.

Например, если:

Если искать текст "кошак" в столбце с такими значениями: "кит", "тигр", "кошка", "крошка", то ВПРнечеткий выдаст "кошка".

Если искать аналогичный текст в столбце с: "кит", "тигр", "крошка", то ВПРнечеткий выдаст "крошка".

Если искать среди: "кит", "тигр", то ВПРнечеткий выдаст "кит".

Т.е. формула требует внимания человека, тем не менее, она способна сильно облегчить труд при приведении списков к стандартному виду.

## А так же 
Доступна используемая внутри формула =Levenshtein

Она возвращает Расстояние Левенштейна (минимальное количество необходимых перестановок символов) одной строки от другой. Т.е. некую меру сходства (чем меньше - тем сходство выше).
