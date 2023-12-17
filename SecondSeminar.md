# Второй семинар
12.12.2023
## Создание веток
git branch branch_name - создание ветки
## Слияние веток
git merge - слияние веток
## Конфликты при слияниях
Конфликты возникают, когда затронуто общее рабочее пространство

Создание конфликта на ветке 1stBranch
## Ветка 1

## + Ветка 2

## + Ветка 3

## + Ветка 4

----
----

# Home work 3

# Работа с удаленными репозиториями в Git

## Клонирование удаленного репозитория

Чтобы начать работу с удаленным репозиторием, нужно его клонировать на локальную машину.

_Команда:_ git clone <URL_удаленного_репозитория>

## Работа с ветками

2.1. Просмотр удаленных веток

_Команда:_ git branch -r

2.2. Просмотр веток

_Команда:_ git branch

2.3. Переключение между ветками

_Команда:_ git checkout <Имя ветки, на которую переключаемся>

2.4. Создание локальной ветки, отслеживающей удаленную ветку

_Команда:_ git checkout -b <название_новой_ветки> origin/<название_удаленной_ветки>

2.5. Слияние веток

_Команда:_ git merge

## Получение изменений из удаленного репозитория

3.1. Получение изменений без слияния (fetch)

_Команда:_ git fetch

3.2. Получение и автоматическое слияние изменений (pull)

_Команда:_ git pull origin <название_удаленной_ветки>

## Отправка изменений на удаленный репозиторий

4.1. Загрузка изменений в ветку, отслеживающую удаленную ветку

_Команда:_ git push origin <название_локальной_ветки>

## Работа с несколькими удаленными репозиториями

5.1. Просмотр списка удаленных репозиториев

_Команда:_ git remote -v

5.2. Добавление нового удаленного репозитория

_Команда:_ git remote add <название_удаленного_репозитория> <URL_удаленного_репозитория>

5.3. Загрузка изменений в другой удаленный репозиторий

_Команда:_ git push <название_удаленного_репозитория> <название_локальной_ветки>

## Удаление и переименование удаленных веток

6.1. Удаление удаленной ветки

_Команда:_ git push origin --delete <название_удаленной_ветки>

6.2. Переименование удаленной ветки

_Команда:_ git push origin :<старое_название_ветки> <новое_название_ветки>