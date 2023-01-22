# Инструкция для работы с Git и удалёнными репозиториями

# Что такое Git?

Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.

# Подготовка репозитория

Для создание репозитория необходимо выполнить команду _git init_ в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

# Создание коммитов

## Git add

Для добавления измений в коммит используется команда _git add_. Чтобы использовать команду _git add_ напишите _git add <имя файла>_

## Просмотр состояния репозитория

Для того, чтобы посмотреть состояние репозитория используется команда _git status_. Для этого необходимо в папке с репозиторием написать _git status_, и Вы увидите были ли измения в файлах, или их не было.

## Создание коммитов

Для того, чтобы создать коммит(сохранение) необходимо выполнить команду _git commit_. Выполняется она так: _git commit -m "<сообщение к коммиту>_. Все файлы для коммита должны быть **_ДОБАВЛЕНЫ_** и сообщение к коммиту писать **_ОБЯЗАТЕЛЬНО_**.

# Перемещение между сохранениями

Для того, чтобы перемещаться между коммитами, используется команда _git checkout_. Используется она в папке с пепозиторием следующим образом: _git checkout <номер коммита>_

# Журнал изменений

Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда _git log_. Для этого достаточно выполнить команду _git log_ в папке с репозиторием

# Ветки в Git

## Создание ветки

Для того, чтобы создать ветку, используется команда _git branch_. Делается это следующим образом в папке с репозиторием: _git branch <название новой ветки>_

# Слияние веток

Для того чтобы дабавить ветку в текущую ветку используется команда _git merge_

# Удаление веток

Для удаления ветки ввести команду _"git branch -d 'name branch'"_

# Добавление картинок

## Картинка

![Frog](lyagushka.jpg)

## Гифка

![yellow frog](giphy.gif)

## Картинка через сылку в интернете

![Red eyes frog](https://cdn.britannica.com/70/161670-050-8E5BCC80/Red-eyed-tree-frog.jpg)

## Рабщта с ветками

- Для того, чтобы открыть меню со списком веток, следуепт прописать команду _git branch_
- Для того, чтобы создать новую ветку, прописывается команда _git branch **Любое название, которое вы захотите для вашего удобства**_
- Чтобы переместиться на нужную ветку, прописывается еоманда _git chekout_ и название самой ветки

Проверочный пункт для попытки слияние дополнительных веток с уже написанной информацией в блоке на этих же строчках

- Для того, чтобы слить уже готовую ветку с основной частью, необходимо прописать команду _git merge_
- В случае, если при слияние возник конфликт, то необходимо провести анализ. Программа предложи обе версии файл с изменениями, что были внесены после слияния. Сравних их, можно будет принять новую версию, оставить стараю или проветси их комбинацию

# Удаление веток

Для того, чтобы провести удаление ветки, необходимо к команде _git branch_ добавить элемент _-d_, а после уже название ветки, которую вы хотите удалить
Например: _git branch -d **Название ветки**_
