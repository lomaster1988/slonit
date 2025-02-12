# Базовые команды взаимодействия с GIT

## Конфигурация

**git config user.name “<имя_фамилия>”** - установка автора

**git config user.email “<e-mail>”** - установка e-mail

**.cat git/config** - отобразить содержимое файла

**git config –list** - значения параметров конфигурации
**git config –list —global** - только глобальные
**git config –-global alias.c config** - сделать алиас на <c> (git -c --list)

**git init** – создание пустого git-репозитория (/.git в корне проекта)

**git status** - взгляд со стороны на файлы нашего проекта

## Добавление

**git add <название файла>** - проиндексировать файл

** git add . ** - передать в git add весь текущий каталог

**git add -p <название файла>** - по каждому измененному фрагменту (добавлять или нет)

*иногда используется .gitkeep – файл нулевого размера для добавления пустых каталогов в git add*

*.gitignore – файл в корне проекта для указания игнорируемых директорий*

*git add –force <название файлы>* - заставить git добавить файл в индекс, которые находится в gitignore


**git reset HEAD <назвние каталога>** - сбрасывает изменения в индексе для указанного каталога

**git commit** - сделать коммит

** git commit –-author = ‘John Smith <John@me.com>’ --date=’…’ ** - сделать коммит с флагами (указание автора и дату, вместе с коммитером и текущей датой)

**git commit -a** - добавить файлы сразу в коммит с индексированием (кроме неотслеживаемых файлов)

**git commit <пути>** - добавить все файлы в коммит, но лишь для указанных путей

**alias.commitall ‘!git add .; git commit’** - добавление все, включая непроиндексированные (для текущей директории)

** git commit -m ‘<параметры>’ ** - коммит с флагом параметров (переименовать и пр.)
## Посмотреть коммиты

**git show** - посмотреть коммит

**git show <идентификатор> --pretty=fuller** - посмотреть коммит

## Удаление и переименовывание

**git rm <пути>** - удаление с диска и добавление информации об этом в git add
**флаг -r** - удаление из директории
**флаг -f** - удаление файлов с изменениями, которые не были сохранены в репозитории
**--cached** - тольки из индекса

**git mv <old><new>** - переименовывает в рабочей директории и добавляет инф. об этом в индекс
