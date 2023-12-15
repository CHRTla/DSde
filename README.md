# Домашнее задание #3
## Работа с удаленными репозиториями.

Скачивание из текущего репозитория и слияние со своей версией.
Освоить работу с удаленными репозиториями, которые находятся не на локальной, а на удаленной машине, например, на сервере.
Копировать внешний репозиторий на свой ПК можно командой `git clone https://....`.

Команда `git clone` составная: она не только загружает все изменения, но и пытается слить все ветки на локальном компьютере и в удаленном репозитории.

`git pull` - Эта команда позволяет скачать все из текущего репозитория и автоматически сделать **merge** с нашей версией

`git push` - Отправить свою версию репозитория во внешний репозиторий. 

`pull request` - команда для предложения изменений, запрос на вливание изменений в сторонний репозиторий

## Как сделать pull request

- Делаем (ответвление) репозитория fork
- Делаем `git clone` СВОЕЙ версии репозитория
- Создаем новую ветку (`git branch new_branch`) и **в НЕЕ** вносим свои изменения
- Фиксируем изменения (делаем коммиты)
- Отправляем свою версию в свой GitHub (`git push`)
- На сайте GitHub нажимаем кнопку pull request