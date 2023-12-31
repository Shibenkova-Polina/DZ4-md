# Шпаргалка по регулярным выражениям

- ### Метасимволы
Символ обратной косой черты (\\) указывает на то, что символ, следующий за ним, является специальным символом<br>
`\d` Любая цифра (эквивалентно [0-9]) <br>
`\D` Любой символ, кроме цифр <br>
`\s` Символ пробела <br>
`\S` Любой символ, кроме пробела <br>
`\w` Символы, соответствующие словам, сокращение от [a-zA-Z_0-9] <br>
`\W` Символы, не образующие слов, сокращение от [^a-zA-Z_0-9] <br>

- ### Квантификаторы
Квантификаторы определяют частоту появления элемента <br>
`*`	Ноль или более раз, сокращение от {0,} <br>
`*` Один или более раз, сокращение {1,} <br>
`?` Один или ноль раз, сокращение {0,1}<br>
`{X}`  X раз <br>
`{X,}`  X и более раз <br>
`{X,Y}`	Не менее X, но не более Y раз <br>
`*?` ? после квантификатора делает его ленивым. Он пытается найти наименьшее совпадение. Это останавливает регулярное 
выражение при первом совпадении <br>

- ### Классы символов
Класс символов будет соответствовать любому из набора символов <br>
`[abc]` Любой символ из набора a, b, c <br>
`[^abc]` Любой символ, кроме a, b, c <br>
`[a-z]` Любой символ в диапазоне от a до z <br>
`[a-d1-7]` Любая буква в диапазоне от a до d и любая цифра в диапазоне от 1 до 7 <br>
`X|Y` X или Y

- ### Якоря
`$`	Конец строки <br>
`^`	Начало строки<br>
`^regex`	Поиск регулярного выражения с совпадением в начале строки <br>
`regex$`	Поиск регулярного выражения с совпадением в конце строки <br>

- ### Классы регулярных выражений
Обработку регулярных выражений поддерживают два класса: Pattern и
Matcher, которые работают вместе. <br>
`java.util.regex.Pattern` используется для определения шаблонов, для создания которго нужно использовать
метод `compile()`. <br>
`java.util.regex. Matcher` интерпретирует шаблон регулярного выражения и
осуществляет операции сопоставления для входной строки путём вызова метода `matcher()`. <br>

Чтобы получить результат работы написанного регулярного выражения,
нужно воспользоваться методом `find()`, осуществляющим поиск нескольких
вхождений выражения в тексте, или использовать метод `matches()`, который
возвращает true только тогда, когда весь текст соответствует заданному
регулярному выражению.
