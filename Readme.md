# Инструкция для работы с Git и удалёнными репозиториями
# Что такое Git?
Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.
# Подготовка репозитория
Для создание репозитория необходимо выполнить команду _git init_ в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

# Создание коммитов
## Git add
Для добавления измений в коммит используется команда *git add*. Чтобы использовать команду git add напишите *git add <имя файла>*

Просмотр состояния репозитория
---
Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого необходимо в папке с репозиторием написать *git status*, и Вы увидите были ли измения в файлах, или их не было.

## Создание коммитов
Для того, чтобы создать коммит(сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "<сообщение к коммиту>*. Все файлы для коммита должны быть ***ДОБАВЛЕНЫ*** и сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***.

# Добавление картинок
## Картинка
   ![картинки](https://miro.medium.com/max/1400/1*vlDY5078rLn0dFQWbdAKUA.png)
## Гифка
   ![гиф](https://raw.githubusercontent.com/nadehi18/battery-wallpaper-windows/master/preview/charging.gif)
## Картинка из папки
   ![картинка](1_S-_fv45WT4MgqtnPVsxtHQ.jpeg)

# Перемещение между сохранениями
Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с пепозиторием следующим образом: *git checkout <номер коммита>*
# Слияние веток
Для того чтобы дабавить ветку в текущую ветку используется команда *git merge*
# Журнал изменений
Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда _git log_. Для этого достаточно выполнить команду _git log_ в папке с репозиторием
# Ветки в Git
Создание ветки
Для того, чтобы создать ветку, используется команда *git branch*. Делается это следующим образом в папке с репозиторием: *git branch <название новой ветки>*

смотрим команду git commit -am "save all"

## Начало работы

Создание нового репозитория, первый коммит, привязка удалённого репозитория с gthub.com, отправка изменений в удалённый репозиторий.

# указана последовательность действий:
# создана директория проекта, мы в ней
git init                      # создаём репозиторий в этой директории
touch readme.md               # создаем файл readme.md
git add readme.md             # добавляем файл в индекс
git commit -m "Старт"         # создаем коммит
git remote add origin https://github.com:nicothin/test.git # добавляем предварительно созданный пустой удаленный репозиторий
git push -u origin master     # отправляем данные из локального репозитория в удаленный (в ветку master)

## Клонирование репозитория

# клонировать удаленный репозиторий в одноименную директорию
git clone https://github.com/cyberspacedk/Git-commands.git    

# клонировать удаленный репозиторий в директорию «FolderName»
git clone https://github.com/cyberspacedk/Git-commands.git FolderName 

# клонировать репозиторий в текущую директорию
git clone https://github.com:nicothin/web-design.git .   

# Пример:
$ git clone git@github.com:ifireiceya/MyFirstRepo.git
Cloning into 'MyFirstRepo'...
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (4/4), done.

Переходим в новый каталог, где теперь лежит копия нашего проекта с GitHub:

$ cd MyFirstRepo

## Синхронизация репозитория-форка с мастер-репозиторием

Есть некий репозиторий на github.com, он него нами был сделан форк, добавлены какие-то изменения. Оригинальный (мастер-)репозиторий был как-то обновлён. Задача: стянуть с мастер-репозитория изменения (которые там внесены уже после того, как мы его форкнули).

# Форк
Форк (Fork) — собственное ответвление (fork) какого-то проекта. Это означает, что GitHub создаст вашу собственную копию проекта, данная копия будет находиться в вашем пространстве имён, и вы сможете легко делать изменения путём отправки (push) изменений.

# указана последовательность действий:
git remote add upstream https://github.com:address.git # добавляем удаленный репозиторий: сокр. имя — upstream, URL мастер-репозитория
git fetch upstream            # стягиваем все ветки мастер-репозитория, но пока не сливаем со своими
git checkout master           # переключаемся на ветку master своего репозитория
git merge upstream/master     # вливаем стянутую ветку master удалённого репозитория upstream в свою ветку master

## Отправка изменений на GitHub

Чтобы отправить изменения на GitHub (сделать push), нужно определить имя удаленного репозитория.

$ git remote

Имя данного удаленного репозитория — «origin».

После определения имени можно безопасно отправить изменения на GitHub.

git push origin [Branch Name]

## Создание пул-реквеста

Перейдите в свой репозиторий на GitHub. Там есть кнопка «Compare & pull request» — кликните ее.


Введите необходимые детали относительно того, что именно вы сделали (чтобы поставить ссылку на issues, возпользуйтесь знаком «решетки»). После этого можно нажать кнопку подтверждения внизу.


Поздравляю! Вы создали свой первый пул-реквест. Если его примут, вы получите уведомление по электронной почте.