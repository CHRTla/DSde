# Домашнее задание #3

# Инструкция по работе с контролем версий
## 4 шага работы с контролем версий
* внести изменения
* сохранить изменения (CTRL+S)
* добавить файл с изменениями (git add file_name)
* зафиксировать эти изменения (git commit -m "Comment")
## gin init - инициализировать локальный репозитарий
## git add - добавить файл, можно сохранить определенный файл, набрав его имя в конце с расширением или найти его при помощи TAB (git add FirstSeminar.md, например), либо сохранить все файлы в папке, поставив точку через пробел (git add .) 
## git version - узнать верию гита
## git diff - узнать разницу между сохраненным файлом и зафиксированным
## git commit - фиксация изменений
## git commit -m "comment" - фиксация измнений с комментарием
## git commit --amend -m "new_comment" - замена комментария, для этого нужно сначала перейти на нужный коммит
## git log - вывести историю изменений
## git log --graph - история изменений в графическом виде (показываются разные ветки, из слияние)
## git checkout - переход к определенному коммиту, в конце указываются минимум 4 первые цифры нужного коммита. Также можно использовать для перехода между ветками, тогда в конце указывается название ветки (branch_name)
## git branch - выводит список имеющихся веток (звёздочкой (*) отмечена текущая ветка)
## git branch branch_name - создание новой ветки
## git branch -d branch_name - удаление ветки (если в ветке есть информация, и она не была слита с другой веткой, то удаление невозможно)
## git branch -D branch_name - удаление любой ветки, даже с имеющейся в ней инфорамцией, если ветка не была слита с другой
## git merge branch_name - слияние веток. Слияние произойдёт в текущей ветке, инфорамция в неё будет доавлена из указанной ветки. Слияние может пройти автоматически или с конфликтами, которые нужно разрешить. Конфликт возникает, если в файлах затрагивается одно рабочее пространство, тогда нужно выбрать одну из имеющихся опций (принять версию текущей ветки, принять версию из сливаемой ветки, принять оба изменения или сравнить измнения).
## Выделение текста

Чтобы выделить текст курсивом, его необходимо обрамить звёздочками (*) или знаком нижнего подчёркивания (_). Например, *вот так* или _вот так_.

Чтобы выделить текст полужирным, его необходимо обрамить двойными звёздочками (**) или двойным занком нижнего подчёркивания (__). Например, **вот так** или __вот так__.

Альтернативные способы выделения текста жирным или курсивом нужны для того, чтобы мы могли совмещать оба этих способа. Например, _текст может быть выделен курсивом и при этом быть **полужирным**_.
## Работа со списками
Чтобы добавить ненумерованный список, необходимо пункты выделить звёздочкой (*) или знаком (+). Например, вот так:
* Элемент 1
* Элемент 2
* Элемент 3
+ Элемент 4

Чтобы добавить нумерованные списки, необходимо пункты просто пронумеровать. Например, вот так:
1. Первый пункт
2. Второй пункт
## Работа с изображениями

Чтобы вставить изображение в текст, достаточно написать следующее: ![Привет, Это Турурушка](tururu.jpg) Где [альтернативный текст, если изображение не откроется], а (файл с изображением)

# Работа с удалёнными репозиториями

Смысл работы с контролем версий - возможность одновременной работы над проектом нескольких участников, для реализации этого как раз используются удалённые репозитории. Одним из наиболее популярных является сервис GitHub.

При создании локального репозитория можно использовать команду git init, тогда будет создан собственный локальный репозиторий, который затем можно перенести в удалённый репозиторий. Либо можно использовать команду git clone (link), тогда в локальный репозиторий будет скопирован собственный или чужой удалённый репозиторий.

## Копирование локального репозитория в удалённый
Все команды набираются в терминале локального репозитория
git remote add origin (your_github_account_link/repository_name.git) - создание удалённого репозитория
git branch -M main (or master) - создаём главную ветку в удалённом репозитории
git push -u origin main (or master) - отправляем информацию в удалённый репозиторий, при этом имя главной ветки в данной строке и предыдущей должны совпадать, это может быть main или master (хотя ветка принципиально может называться как угодно, но как правило используют эти названия, чтобы не вносить путаницу в совместную работу)

## Копирование удалённоего репозитория в локальный
## git clone (link) - копирование удалённого репозитория в локальный репозиторий
## cd (folder_name) - перемещение между папками в локальном репозитории

## git push - отправка локального репозитория в удалённый (у команды могут быть дополнительные параметры, нужно следовать подсказкам, которые показывает терминал при наборе команды)
## git pull - получение актуальной версии с обновлениями с GitHub и слияние с текущей веткой


