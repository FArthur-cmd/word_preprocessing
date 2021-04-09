# Задача

>В огромном тексте содержится тайный шифр. Чтобы его прочитать, необходимо взять слово-ключ (которое может быть самым разным, но не превышает по длине пяти букв) и найти последовательность из нескольких слов таких, что первая буква первого слова, вторая -- второго, третья -- третьего и так далее будут образовывать слово-ключ. Номер первого слова необходимо вывести.
>
>Реализуйте структуру, которая принимает текст, обрабатывает его, а потом эффективно отвечает на запросы, возвращая номер первого слова по ключу. Слова разделены пробелами и переводами строк, символы не учитываются. Если подходящих последовательностей несколько, выведите любой из ответов.
>
>Например, текст -- это задание, ключ -- “чек”, ответ -- 31
>
>Текст представляет из себя .txt - файл размером до 2ГБ, а запросы и ответы на них должны вводиться/выводиться в консоль.

# Интерфейс решения

При запуске программы необходимо передать ей имя программы (полный путь до файла).

В ходе выполнения программы необходимо передать программе количество желаемых тестов и далее написать их по порядку.
Для каждого теста программа выведет индекс первого слова из группы слов, которые могут образовывать ключ или -1 в случае, если такого вхождения в тексте нет.

Особенности реализации (файлы должны содержать английский язык, то есть подчиняться стандартному считыванию с++).

Асимптотика:
* Добавление слова и его создание `O(длинна слова)` (в нашем случае `O(5) = O(1)`).
* Поиск имеет асимптотику `O(длинна слова)`.
* **Итоговая асимптотика:** `O(n*k+m*k)`, где `n` - количество слов в тексте, `k` - длина ключа, `m` - количество запросов.

В папочки для тестов запускаем файл `.sh` в папке должен находиться бинарный файл. (Небольшие размеры ключей для частого попадания).