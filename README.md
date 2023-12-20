# Домашнее задание #3
## Установить git на свою машину очень просто:
* Linux — нужно просто открыть терминал и установить приложение при помощи пакетного менеджера вашего дистрибутива. Для Ubuntu команда будет выглядеть следующим образом:
## sudo apt-get install git
* Windows — мы рекомендуем git for windows, так как он содержит и клиент с графическим интерфейсом, и эмулятор bash.
* OS X — проще всего воспользоваться homebrew. После его установки запустите в терминале:
## brew install git
* Можно скачать по ссылке - <https://git-scm.com/downloads>

# 4  Шага работы с контролем версий:
* Внести изменения
* Сохранить изменения (CTRL + S)
* Добавить файл с изменениями
* Зафиксировать эти изменения
## git init - инициализировать локальный репозиторий
## git add - добавить файл
## git add . - добавить все файлы
## git commit *-m* "комментарий разработчика *«Максимально ясно, просто и содержательно обозначь написанное!»*" - описание закоммиченных изменений
## git commit *--amend -m* "Новый комментарий" - сообщение последнего коммита перезапишется
## git log - содержится вся информация о каждом отдельном коммите и его идентификатор *(навигация по списку стрелочками, для выхода из неё нажимаем "**Q**")*
## git version - узнать версию гита
## git checkout **** - позволяет вернуть выбранный файл к состоянию на момент определенного коммита *(* **** *- первые 4 знака идентификатора нужного коммита)*
## git checkout master - переключаемся на ветку master в последний коммит в ней
## git diff - узнать разницу между сохраненными файлами и зафиксированным файлом
## Создание веток
git branch branch_name - создание ветки
>Важно понимать, что ветки — это просто указатели на коммиты. Когда вы создаете ветку, Git просто создает новый указатель. Репозиторий при этом никак не изменяется.
## Слияние веток
git merge - слияние веток. Команда git merge автоматически выбирает стратегию слияния, если она не указана явным образом. Команды git merge и git pull могут использоваться с параметром -s (стратегия). К параметру -s можно добавить имя стратегии слияния, которую вы хотите использовать. Если стратегия явно не указана, Git выберет подходящую на основе предоставленных веток.
>  **Рекурсивная стратегия** <br> *git merge -s recursive branch1 branch2* <br> Эта стратегия работает с двумя указателями HEAD. Она применяется по умолчанию при выполнении команды pull или merge для одной ветки. Рекурсивная стратегия позволяет обнаруживать и обрабатывать слияния с переименованием, но на сегодняшний день не может использовать обнаруженные копии. Эта стратегия применяется по умолчанию при выполнении команд pull или merge для одной ветки.<br><br>
>  **Стратегия «Осьминог»** <br> *git merge -s octopus branch1 branch2 branch3 branchN* <br>Стратегия «Осьминог» применяется по умолчанию для более чем двух голов. Когда передается больше одной ветки, «осьминог» включается автоматически. Если в слиянии есть конфликты, которые нужно разрешать вручную, эта стратегия блокирует попытку слияния. В основном она используется для объединения голов аналогичных функциональных веток.<br><br>
> **Стратегия «Наша»** <br> *git merge -s ours branch1 branch2 branchN* <br> Стратегия «Наша» (Ours) позволяет работать с множеством веток. Выходной результат слияния всегда соответствует указателю HEAD текущей ветки. Эта стратегия называется «Наша», потому что она игнорирует все изменения из «чужих» веток. Ее назначение — объединение истории аналогичных функциональных веток.<br><br>
> **Стратегия «Поддерево»** <br> *git merge -s subtree branchA branchB* <br>Это разновидность рекурсивной стратегии. При слиянии A и B, если B — дочернее поддерево A, сначала обновляется B, чтобы отразить древовидную структуру A. Кроме того, обновляется родительское дерево, которое является общим для A и B.
## Конфликт при слиянии
Возникают когда, мы затрагиваем общее рабочее пространство при git merge
>Git прерывает работу в самом начале слияния, если Git обнаруживает изменения в рабочем каталоге или разделе проиндексированных файлов текущего проекта. Git не может выполнить слияние, поскольку иначе эти ожидающие изменения будут перезаписаны новыми коммитами. Такое случается из-за конфликтов не с другими разработчиками, а с ожидающими локальными изменениями. Локальное состояние необходимо стабилизировать с помощью команд git stash, git checkout, git commit или git reset. Если команда слияния прерывается в самом начале, выдается сообщение об ошибке.
## Работа с чужим проектом и Pull requests в него
1. На странице проекта в **GitHub** нажимаем конпку (Fork) - проект копируется к вам в **GitHub** ( в Repositori name* прописываем уникальное для нашего рипозитория имя и прописываем Discription)
2. В нашем **GitHub** нажимаем кнопку (<>Code) и копируем ссылку для клонирования -> в VSCode в терминале пишем <br>
*git clone ссылка на наш репозиторий* -> появится папка с проектом
3. Переходим в папку проекта в терминале: *cd название папки в которую нужно перейти*
4. Создаём рабочую ветку и переходим в неё в терминале: <br>
*git branch название ветки*<br>
*dit checkout название ветки*
5. Вносим наши изменения
6. После внесения изменений сохраняем файл -> В терминале:<br>
*git add* .<br>
*git commit -m "коммит"*
7. Пушим изменения -в терминале:<br>
*git push* -> выдаёт ошибку потому что мы не определили тип связи + выдаст подсказку<br>
*git push --set -upstream ...*<br>
можно скопировать и ввести в терминал, тем самым создав удалённую версию нашей локальной версии
8. Открываем **GitHub** и обнавляем, отабразится две ветки в нашем проекте и появилась возможность отправить **Pull requests**
9. Нажимаем кнопку (Compare & Pull requests) -> выйдет окно:
Add a title - последний коммит который мы сделали
Add a discription - дополнительное описание, если нужен большой текст прописать
10. Нажимаем на кнопку (Create pull request) -> Возвращает в репозиторий автора