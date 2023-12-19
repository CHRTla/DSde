# Инструкция для работы с Markdown

## Выделение текста


Чтобы выделить текст курсивом необходимо обрамить его звездочками (*) или знаком нижнего подчеркивания (_). Например, *вот так* или _вот так_  .

Чтобы выделить текст полужирным, необходимо обрамить его двойными звездочками (**)или двойным знаком нижнего подчеркивания(__). Например, **вот так** или __вот так__.

Чтобы зачеркнуть текст, нужно использовать две тильды (~~) . Например, ~~вот так~~ .

Альтернативные способы выделения текста жирным или курсивом нужны для того чтобы совмещать обаэтих способа. Например, _текст может быть выделен курсивом и при этом быть **полужирным**_ .

## Списки

Чтобы добавить ненумерованные списки, необходимо пункты выделить звездочкой (*). Например, вот так:
* Элемент 1
* Элемент 2
* Элемент 3

Чтобы добавить нумерованные списки необходимо просто пронумеровать. Например, вот так:
1. Первый пункт
2. Второй пункт

## Работа с изображениями

Чтобы вставить изображение в текст, достаточно написать следующее:
![Это Git](git.jpg)

## Ссылки

Чтобы поместить ссылку в Markdown, необходимо заключить её в угловые скобки (<>). Например: <https://gb.ru/> .

## Работа с таблицами

В языке Markdown есть возможность оформлять таблицы. Столбцы разделяются вертикальными линиями (|), а строка с шапкой отделяются от остальных дефисами (-), которых можно ставить сколько угодно. Например:
|Столбец 1|Столбец 2|Столбец 3|
|-|--------|---|
|Длинная запись в первом столбце|Запись во втором столбце|Запись в третьем столбце|
|Кртк зпс| |Слева нет записи|

Чтобы выровнять весь столбец по правому краю, в строке с дефисами сразу после дефисов можно поставить двоеточие(:). Чтобы выровнять содержимое по центру, надо поставить двоеточие с обеих сторон.
Например:
|Столбец 1|Столбец 2|Столбец 3|
|:-|:-:|-:|
|Равнение по левому краю|Равнение по центру|Равнение по правому краю|
|Запись|Запись|Запись
|
## Цитаты

Чтобы параграф отобразился как цитата, нужно поставить перед ним закрывающуюся скобку (>).
Например: 
>Оформление цитатой.

# Инструкция для работы с удаленными репозиториями

Репозитории бывают открытые и закрытые. Для работы с чужим открытым репозиторием необходимо:
- на github создать fork необходимого репозитория
- выполнить команду *git clone <fork_url>* (желательно по https)
- добавить необходимые файле через команду через *git add <file_name>*
- команда *git pull* позволит получить свежие изменение, если они есть
- выполнить команду *git commit -m "<Комментарий к коммиту>"*
- выполнить команду *git push*
- открыть Git, убедиться в наличии изменений
- перейти в необходимый репозиторий, откуда было сделано ответвление и нажать *Create pull request*
- выбрать интересующие base repository (оригинальный репозиторий) и head repository (ответвление) и сравнить изменения
- добавить комментарий к запросу на слияние и нажать *Create pull request*

## Команды при работе с удаленными репозиторями

* git clone - используется для создания локальной копии удаленного репозитория Git. Это позволяет вам получить копию проекта на вашем локальном компьютере и начать работу с ним.

* git push - используется для отправки изменений из вашего локального репозитория в удаленный репозиторий Git. Это позволяет обновить содержимое удаленного репозитория на основе ваших локальных изменений. 
Помимо базового синтаксиса, команда git push имеет несколько флагов, которые можно использовать для дополнительной настройки:

-u или --set-upstream - устанавливает отслеживание для ветки, что позволяет вам использовать git push и git pull без указания имени удаленного репозитория и названия ветки;
-f или --force - заставляет Git принудительно заменить удаленную ветку измененной локальной веткой, даже если это приведет к потере данных;
-n или --dry-run - позволяет вам протестировать команду git push, не отправляя реальных изменений в удаленный репозиторий;
-v или --verbose - выводит дополнительную информацию о процессе отправки изменений.

* git fetch - используется для получения изменений из удаленного репозитория Git, но не вносит изменения в локальную ветку. Эта команда позволяет вам получить информацию о ветках и коммитах, которых еще нет в локальном репозитории.

* git pull - используется для получения изменений из удаленного репозитория и объединения их с вашей локальной веткой.

## Заключение