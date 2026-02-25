# Этот файл содержит шпаргалку с базовыми командами для работы c git bash

---

## Навигация

* pwd (от англ. <strong><em>p</em></strong><em>rint <strong>w</strong>orking <strong>d</strong>irectory</em>, «показать рабочую папку») — покажи, в какой я папке;

* ls (от англ. <strong><em>l</em></strong><em>i<strong>s</strong>t directory contents</em>, «отобразить содержимое директории») — покажи файлы и папки в текущей папке;

* ls -a — покажи также скрытые файлы и папки, названия которых начинаются с символа .;

* cd first-project (от англ. <strong><em>c</em></strong><em>hange <strong>d</strong>irectory</em>, «сменить директорию») — перейди в папку first-project;

* cd first-project/html — перейди в папку html, которая находится в папке first-project;

* cd .. — перейди на уровень выше, в родительскую папку;

* cd ~ — перейди в домашнюю директорию (/Users/Username);

* cd / — перейди в корневую директорию.

## Работа с файлами и папками

### Создание

* touch index.html (англ. touch, «коснуться») — создай файл index.html в текущей папке;

* touch index.html style.css script.js — если нужно создать сразу несколько файлов, можно напечатать их имена в одну строку через пробел;

* mkdir second-project (от англ. <strong><em>m</em></strong><em>a<strong>k</strong>e <strong>dir</strong>ectory</em>, «создать директорию») — создай папку с именем second-project в текущей папке.

### Копирование и перемещение

* cp file.txt ~/my-dir (от англ. <strong><em>c</em></strong><em>o<strong>p</strong>y</em>, «копировать») — скопируй файл в другое место;

* mv file.txt ~/my-dir (от англ. <strong><em>m</em></strong><em>o<strong>v</strong>e</em>, «переместить») — перемести файл или папку в другое место.

### Чтение

* cat file.txt (от англ. <em>con<strong>cat</strong>enate and print</em>, «объединить и распечатать») — распечатай содержимое текстового файла file.txt.

### Удаление

* rm about.html (от англ. <strong><em>r</em></strong><em>e<strong>m</strong>ove</em>, «удалить») — удали файл about.html;

* rmdir images (от англ. <strong><em>r</em></strong><em>e<strong>m</strong>ove <strong>dir</strong>ectory</em>, «удалить директорию») — удали папку images;

* rm -r second-project (от англ. <strong><em>r</em></strong><em>e<strong>m</strong>ove,</em> «удалить» + <strong><em>r</em></strong><em>ecursive</em>, «рекурсивный») — удали папку second-project и всё, что она содержит.

## Head
* Файл HEAD (англ. «голова», «головной») — один из служебных файлов папки .git. Он указывает на коммит, который сделан последним (то есть на самый новый).
* Внутри HEAD — ссылка на служебный файл: refs/heads/master (или refs/heads/main в зависимости от названия ветки)

## Статусы untracked/tracked, staged и modified
Одна из ключевых задач Git — отслеживать изменения файлов в репозитории. Для этого каждый файл помечается каким-либо статусом. Рассмотрим основные.

* <strong>untracked (англ. «неотслеживаемый»). </strong> Новые файлы в Git-репозитории помечаются как untracked, то есть неотслеживаемые. Git «видит», что такой файл существует, но не следит за изменениями в нём.  У untracked-файла нет предыдущих версий, зафиксированных в коммитах или через команду git add.

* <strong> staged (англ. «подготовленный»). </strong> После выполнения команды git add файл попадает в staging area (от англ. stage — «сцена», «этап [процесса]» и area — «область»), то есть в список файлов, которые войдут в коммит. В этот момент файл находится в состоянии staged.

* <strong> tracked (англ. «отслеживаемый»). </strong> Состояние tracked — это противоположность untracked. Оно довольно широкое по смыслу: в него попадают файлы, которые уже были зафиксированы с помощью git commit, а также файлы, которые были добавлены в staging area командой git add. То есть все файлы, в которых Git так или иначе отслеживает изменения.

* <strong> modified (англ. «изменённый»). </strong>  Состояние modified значит, что Git сравнил содержимое файла с последней сохранённой версией и нашёл отличия. Например, файл был закоммичен и после этого изменён.
