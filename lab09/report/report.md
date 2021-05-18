---
# Front matter
lang: ru-RU
title: "Шаблон отчёта по лабораторной работе № 9"
subtitle: "Операционные Системы"
author: "АДОЛЕ ФЕЙТ"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Познакомиться с операционной системой Linux. Получить практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.

# Задание

# Задача 1. Создайте новый файл с помощью vi

# 1. Создайте каталог с именем ~ / work / os / lab06.
2. Перейдите во вновь созданный каталог.
3. Вызовите vi и создайте файл hello.sh
vi hello.sh
4. Нажав кнопку i, введите следующий текст.
#! / bin / bash
АД = Привет
function hello {
МЕСТНОЕ ПРИВЕТСТВИЕ = Мир
echo $ HELLO
}
echo $ HELLO
Привет
5. После ввода текста нажмите Esc, чтобы войти в командный режим.
6. Нажмите «:», чтобы перейти в режим последней строки, и на экране появится двоеточие.
7. Нажмите w (запись) и q (выход), затем нажмите Enter, чтобы сохранить текст и выйти.
8. Сделайте файл исполняемым.
chmod + x hello.sh

# Задание 2. Редактирование существующего файла
1. Вызовите vi на редактирование файла
	vi ~/work/os/lab06/hello.sh
2. Установите курсор в конец слова HELL второй строки.
3. Перейдите в режим вставки и замените на HELLO. Нажмите ``Esc`` для возврата в командный режим.
4. Установите курсор на четвертую строку и сотрите слово LOCAL.
5. Перейдите в режим вставки и наберите следующий текст: local, нажмите ``Esc`` для возврата в командный режим.
6. Установите курсор на последней строке файла. Вставьте после неё строку, содержащую следующий текст: echo $HELLO.
7. Нажмите ``Esc`` для перехода в командный режим.
8. Удалите последнюю строку.
9. Введите команду отмены изменений ``u`` для отмены последней команды.
10. Введите символ ``:`` для перехода в режим последней строки. Запишите произведённые изменения и выйдите из vi.


# Выполнение лабораторной работы



# Выводы

Познакомился с операционной системой Linux.А также, я получил практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.

# Контрольные вопросы
1. Редактор vi имеет три режима работы:
- командный режим — предназначен для ввода команд редактирования и навигации по редактируемому файлу;
- режим вставки — предназначен для ввода содержания редактируемого файла;
-  режим последней (или командной) строки — используется для записи изменений в файл и выхода из редактора.
2. Можно нажимать символ q (или q!), если требуется выйти из редактора без сохранения.
3. Команды позиционирования:
- 0 (ноль) — переход в начало строки;
- $ — переход в конец строки;
- G — переход в конец файла;
- n G — переход на строку с номером n
4. Редактор vi предполагает, что слово - это строка символов, которая может включать в себя буквы, цифры и символы подчеркивания. 
5. G — переход в конец файла
6. Команды редактирования:
- Вставка текста
– ``а`` — вставить текст после курсора;
– ``А`` — вставить текст в конец строки;
– ``i`` — вставить текст перед курсором;
– n ``i`` — вставить текст n раз;
– ``I`` — вставить текст в начало строки.
- Вставка строки
– ``о`` — вставить строку под курсором;
– ``О`` — вставить строку над курсором.
- Удаление текста
– ``x`` — удалить один символ в буфер;
– ``d`` ``w`` — удалить одно слово в буфер;
– ``d`` ``$`` — удалить в буфер текст от курсора до конца строки;
– ``d`` ``0`` — удалить в буфер текст от начала строки до позиции курсора;
– ``d`` ``d`` — удалить в буфер одну строку;
– n ``d`` ``d`` — удалить в буфер n строк.
- Отмена и повтор произведённых изменений
– ``u`` — отменить последнее изменение;
– ``.`` — повторить последнее изменение.
- Копирование текста в буфер
– ``Y`` — скопировать строку в буфер;
– n ``Y`` — скопировать n строк в буфер;
– ``y`` ``w`` — скопировать слово в буфер.
- Вставка текста из буфера
– ``p`` — вставить текст из буфера после курсора;
– ``P`` — вставить текст из буфера перед курсором.
- Замена текста
– ``c`` ``w`` — заменить слово;
– n ``c`` ``w`` — заменить n слов;
– ``c`` ``$`` — заменить текст от курсора до конца строки;
– ``r`` — заменить слово;
– ``R`` — заменить текст.
- Поиск текста
– ``/`` текст — произвести поиск вперёд по тексту указанной строки символов текст;
– ``?`` текст — произвести поиск назад по тексту указанной строки символов текст.
7. ``$`` — переход в конец строки
8.  ``u`` — отменить последнее изменение
9. Режим последней  строки — используется для записи изменений в файл и выхода из редактора.
10. ``$`` — переход в конец строки
11. Опции редактора vi позволяют настроить рабочую среду. Для задания опций используется команда set (в режиме последней строки):
– : set all — вывести полный список опций;
– : set nu — вывести номера строк;
– : set list — вывести невидимые символы;
– : set ic — не учитывать при поиске, является ли символ прописным или строчным.
12. В редакторе vi есть два основных режима: командный режим и режим вставки. По умолчанию работа начинается в командном режиме. В режиме вставки клавиатура используется для набора текста. Для выхода в командный режим используется клавиша Esc или комбинация Ctrl + c .
13. ![image](https://user-images.githubusercontent.com/74152181/116706733-9bfbd480-a9d6-11eb-873e-34b08c65844e.png)
