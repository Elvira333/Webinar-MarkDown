# Инструкция для работы с Git и удалёнными репозиториями
## Что такое Git?
Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.
## Настройка
Мы установили git, теперь нужно добавить немного настроек. Есть довольно много опций, с которыми можно играть, но мы настроим самые важные: наше имя пользователя и адрес электронной почты. Откройте терминал и запустите команды:
*git config --global user.name "My Name"*
*git config --global user.email myEmail@example.com*
Теперь каждое наше действие будет отмечено именем и почтой. Таким образом, пользователи всегда будут в курсе, кто отвечает за какие изменения — это вносит порядок.
## Подготовка репозитория
Для создание репозитория необходимо выполнить команду *git init* в папке с репозитоgit chechрием и у Вас создаться репозиторий (появится скрытая папка .git)
## Создание коммитов
### Git add
Для добавления измений в коммит используется команда *git add*. Чтобы использовать команду git add напишите *git add <имя файла>*
## Отмена коммита
С помощью команды *git checkout* мы можем перейти к предыдущему коммиту , a1e8fb5, и вернуть репозиторий в состояние, предшествовавшее этому безумному коммиту. Переход к отдельному коммиту переведет репозиторий в состояние открепленного указателя HEAD. Работа при этом перестает принадлежать какой-либо из веток. При открепленном указателе HEAD все новые коммиты будут оставаться без родителя, пока вы не вернете ветки в положенное состояние.
## Просмотр состояния репозитория
Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого необходимо в папке с репозиторием написать *git status*, и Вы увидите были ли измения в файлах, или их не было.
## Создание коммитов
Для того, чтобы создать коммит(сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "<сообщение к коммиту>*. Все файлы для коммита должны быть ***ДОБАВЛЕНЫ*** и сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***. 
Можно добавлять один файл, как написано выше, или вместе - всё сразу: *<git add .>*

Конечно добавлять всё сразу удобнее, чем прописывать каждую позицию отдельно. Однако, тут надо быть внимательным, чтобы не добавить по ошибке ненужные элементы. Если же такое произошло изъять оттуда ошибочный файл можно при помощи команды <git reset:> git reset css/style.css

## Журнал изменений
Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда *git log*. Для этого достаточно выполнить команду *git log* в папке с репозиторием.

# Добавление картинок
## Картинка 
![картинки](https://vkrasnoznamenske.ru/upload/iblock/9f6/y7sew2xmc8sp28hw1mg3wvu0dgrvjcfj.jpg)

## Гиф
![гифка](https://i.gifer.com/zmV.gif)

## Добавление картинки из папки
![картинка_из_папки](turmion_katilot.jpg)

## Перемещение между сохранениями
Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с пепозиторием следующим образом: *git checkout <номер коммита>*

## Ветки в Git
В Git ветка — это отдельная линия разработки. Git checkout позволяет нам переключаться как между удаленными, так и меду локальными ветками. Это один из способов получить доступ к работе коллеги или соавтора, обеспечивающий более высокую продуктивность совместной работы. Однако тут надо помнить, что пока вы не закомитили изменения, вы не сможете переключиться на другую ветку.
### Создание ветки
Для того, чтобы создать ветку, используется команда *git branch*. Делается это следующим образом в папке с репозиторием: *git branch <название новой ветки>*
## Слияние веток
Для того чтобы дабавить ветку в текущую ветку используется команда *git merge*
## Удаление веток
Для удаления ветки ввести команду "git branch -d 'name branch'"
Однако тут есть нюанс: удалить текущую ветку, в которую вы, в данный момент просматриваете - нельзя. Если же вы все-таки попытаетесь это сделать, система отругает вас и выдаст ошибку с таким содержанием:
*Error: Cannot delete branch local_branch_name checked out at название_директории*
## Переключение между ветками
Для этого воспользуемся командой checkout, она принимает один параметр — имя ветки, на которую необходимо переключиться. Для этого нужно ввести команду *git checkout <имя ветки>*
# Работа с удаленным репозиторием
## Клонирование репозитория
Команда *git clone <ссылка>* позволяет скопировать репозиториий из интернета.
Для работы с этим репозиторием создается пустая папка без инициализации, из которой выполняется эта команда.
Затем командой *cd <имя папки>* переходим в папку с клонированным репозиторием.
## Извлечение и загрузка содержимого из удаленного репозитория
Команда *git pull* обновляет локальный репозиторий. Так же происходит слияние с нашим файлом *merge*
## Выгрузка содержимого локального репозитория в удаленный репозиторий
Команда *git push* необходима для публикации выгружаемых локальных изменений в центральном репозитории и используется, чтобы поделиться изменениями, внесенными в локальный репозиторий, с удаленными участниками команды.
