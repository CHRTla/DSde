# Домашнее задание #3 Ильина Степана

## Репозиторий- это хранилище файлов, поддерживающее версионность

## Начало работы
При первом использовании Git необходимо представиться. Для 
этого нужно ввести в терминале 2 команды:
* ***git config --global user.name «Ваше имя английскими буквами» git*** 
* ***config --global user.email ваша почта@example.com***
## 4 Шага работы с контролем версий:
* Внести изменения
* Сохранить изменения (Ctrl+s)
* Добавить файл с изменениями
* Зафиксировать эти изменения
## Команды:
* __git help__ - руководство
* __git init__ - инициализировать локальный репозиторий ука
* __git add__ - добавить версионность, при постановке файла на отслеживание нужно указать название файла вместе с расширением.
* __git restore__ — отменить отслеживание изменений
* __git version__ - узнать версию гита
* __git status__ - показать текущие изменения
* __git checkout__ - переход от одного изменения к другому, достаточно запросить по первым 4 символам нужное изменение, ветку изменения
* __git checkout master__ - вернуться к актуальному состоянию и продолжить работу
* __git diff__ - узнать разницу между сохраненным файлом и зафиксированным
* __git commit -m "message"__ - сохранение коммита и комментария к нему. Первый принято называть "initial commit"
* __git log__ - вывод истории всех изменениий 
* __git log –-graph__ - список коммитов в виде графа/дерева
* __git checkout -b [yourbranchname]__ - создать новую ветку и переключиться на неё
* __git merge (имя сливаемой ветки)__- слияние веток, нужно сначала выбрать основную ветку, потом указать имя сливаемой ветки 
* __git rebase__ - повторное применение коммитов
* __git clone <url-адрес репозитория>__ – клонирование внешнего репозитория на локальный ПК
* __git pull__ – получение изменений и слияние с локальной версией
* __git push__ – отправляет локальную версию репозитория на внешний (публикация локальных коммитов)
* __cherry-pick__
* __reset__ - откат к определенному состоянию
* __revert__
* ***клавиша Q*** - выйти из режима просмотра версий
* ***клавиша TAB*** - перебор последних названий файлов
* ***клавиши "стрелка вверх"/"стрелка вниз"*** - перебор введенных команд
* ***команда clear*** - очистить терминал
* ***HEAD*** - это символическое имя текущего выбранного коммита — это, по сути, тот коммит, над которым мы в данный момент работаем.

## Синтаксис языка Markdown
**Выделение текста**

 * "#" Заголовок – выделение заголовков. Количество символов “#” задаёт уровень заголовка (поддерживается 6 уровней).
* = или - – подчёркиванием этими символами (не менее 3 подряд) выделяют заголовки первого (“=”) и второго (“-”) уровней.
 *  (**)- Полужирное начертание двойными звездочками или  двойным знаком нижнего подчеркивания, например **вот так** или __вот так__
 * (*) Курсивное начертание одинарной звездочкой или  одинарным знаком нижнего подчеркивания, например *вот так* или _вот так_
 * (***) Полужирное курсивное начертание тройными звездочками или  дтройным знаком нижнего подчеркивания, например ***вот так*** или ___вот так___
* ~~Зачёркнутый текст~~

**Списки**
* "*" Строка – ненумерованные списки, символ “*” в начале строки. 
* 1, 2, 3 … – нумерованные списки, например
1. Первый пункт
2. Второй пункт


**Работа с изображениями**
Чтобы вставить изображение в текст, достаточно написать следующее:
![Схема веток из лекции 2](sxema.jpg)

**Ссылки**
* __git fetch__ — обновить ссылки

**Работа с таблицами**
Проверяю работу конфликта.
Перестал выводиться выбор действий при сливании
**Цитаты**

**Заключение**

## Порядок работы на Github.com

. Создали аккаунт на Github.com
2. Создать локальный репозтиторий
3. "Подружить" ваш локальный и удаленный репозиторий. Github при создании нового репозитория подскажет как это можно сделать
4. отправить (push) ваш локальный репозиторий в удаленный , при этом вам, возможно, нужно будет авторизоваться на удаленном репозитории.
5. Провести изменения "с другого компьютера"
6. Выкачать (pull) актуальное состояние из удаленного репозитория

 ## Порядок работы с чужими репозиториями

1. Делаем форк (fork) интересующего нас репозитория
2. Мы делаем git clone своей для нашей версии этого репозитория
3. Мы создаем новую ветку с предлагаемыми изменениями
4. Производим все изменения только в этой ветке/
5. Принято прикладывать файл **README** (капслоком) с описанием изменений
5. Отправляем эти изменения на свой аккаунт (puch) на github
6. В окне на Github появляется возможность отправить pull request
7.  git push --set-upstream origin - связывает локальный и удаленный репозитории