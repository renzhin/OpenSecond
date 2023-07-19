# Базовая инструкция по работе с GIT. Перечень команд


## Подготовительная работа. Команды консоли. Навигация

pwd (от англ. print working directory, «показать рабочую папку») — покажи, в какой я папке;
ls (от англ. list directory contents, «отобразить содержимое директории») — покажи файлы и папки в текущей папке;
ls -a — покажи также скрытые файлы и папки, названия которых начинаются с символа .;
cd first-project (от англ. change directory, «сменить директорию») — перейди в папку first-project;
cd first-project/html — перейди в папку html, которая находится в папке first-project;
cd .. — перейди на уровень выше, в родительскую папку;
cd ~ — перейди в домашнюю директорию (/Users/Username);
cd / — перейди в корневую директорию.


## Подготовительная работа. Команды консоли. Работа с файлами и папками

### Создание

touch index.html (англ. touch, «коснуться») — создай файл index.html в текущей папке;
touch index.html style.css script.js — если нужно создать сразу несколько файлов, можно напечатать их имена в одну строку через пробел;
mkdir second-project (от англ. make directory, «создать директорию») — создай папку с именем second-project в текущей папке.

### Копирование и перемещение

cp file.txt ~/my-dir (от англ. copy, «копировать») — скопируй файл в другое место;
mv file.txt ~/my-dir (от англ. move, «переместить») — перемести файл или папку в другое место.

### Чтение

cat file.txt (от англ. concatenate and print, «объединить и распечатать») — распечатай содержимое текстового файла file.txt.

### Удаление

rm about.html (от англ. remove, «удалить») — удали файл about.html;
rmdir images (от англ. remove directory, «удалить директорию») — удали папку images;
rm -r second-project (от англ. remove, «удалить» + recursive, «рекурсивный») — удали папку second-project и всё, что она содержит.

### скопировать в буфер обмена

$ clip < ~/.ssh/id_rsa.pub

*# для ed25519:*

$ clip < ~/.ssh/id_ed25519.pub


## Инструкция по генерации SSH-ключа

ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub"


## Делаем (создаем) папку репозиторием

Сделать папку репозиторием — git init

Разгитить» папку, если что-то пошло не так, — rm -rf .git

ключ r (от англ. recursive — «рекурсивно») позволяет удалять папки вместе с их содержимым;

ключ f (от англ. force — «заставить») избавит вас от вопросов вроде «Вы точно хотите удалить этот файл? А этот? И этот тоже?».

Проверить состояние репозитория — git status

Подготовить файлы к сохранению — git add

Команда git add --all подготовит к сохранению сразу все файлы.

С помощью git add . можно добавить в репозиторий текущую папку со всеми файлами.

Выполнить коммит — git commit


Отправить на сервер - git push
В первый раз эту команду нужно вызвать с флагом `-u` и параметрами `origin` (имя удалённого репозитория) и `main` или `master` (название текущей ветки). Флаг `-u` свяжет локальную ветку с одноимённой удалённой. Как вы связывали локальный и удалённый репозитории в предыдущем уроке, так же и здесь нужно дополнительно связать ветки.

`$ git push -u origin main *# Если команда приведёт к ошибке, попробуйте # заменить main на master.*`

Привязать удалённый репозиторий к локальному — git remote add

Получить лог — git log --oneline
Получить сокращённый лог — git log --oneline
