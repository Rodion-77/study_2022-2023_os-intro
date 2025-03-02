---
## Front matter
title: "Отчет по Лабораторной работе №2"
subtitle: "Markdown"
author: "Павличенко Родион Андреевич"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Изучить идеологию и применение средств контроля версий. Освоить умения по работе с git.

# Задание

-Сделайте отчёт по предыдущей лабораторной работе в формате Markdown.
– В качестве отчёта просьба предоставить отчёты в 3 форматах: pdf, docx и md (в архиве, поскольку он должен содержать скриншоты, Makefile и т.д.)

                            
# Выполнение лабораторной работы

Переходим в режим суперпользователя, устанавливаем пакет git и пакет ghр

![Установка пакетов git и gh](image/1){#fig:001 width=70%}

Задаем имя и email владельца репозитория (команды 1,2) ,настроим utf-8 (команда 3), зададим имя начальной ветке (команда 4), введем параметры autocrlf и safecrlf (команды 5,6)

![Ввод имени и почты, настройка utf-8, autocrlf,safecrlf](image/2){#fig:002 width=70%}


Создаем ключ ssh размером 4096 бит
![Cоздание ключа SSH](image/3){#fig:003 width=70%}

Создаем ключ по алгоритму ed25519

![Создание ключа ed25519](image/4){#fig:004 width=70%}

Генерируем pgp ключ с определенными параметрами

![Генерация pgp ключа](image/5){#fig:005 width=70%}

Копируем PGP-ключ в буфер обмена и переходим на github, вставляем полученный ключ

![Копирование pgp ключа](image/6){#fig:006 width=70%}

Вводим email и указываем git применять его при подписи коммитов, вводим три команды

![Ввод email для git](image/7){#fig:007 width=70%}

При помощи gh авторизируемся

![Авторизация при помощи gh](image/8){#fig:008 width=70%}

Создаем репозиторий курса на основе шаблона

![Создание репозитория](image/9){#fig:009 width=70%}

![Создание репозитория](image/10){#fig:010 width=70%}

Настраиваем каталог курса, сначала переходим в него (команда 1), далее удаляем лишние файлы (команда 2) и создаем необходимые каталоги (команда3,4)

![Настройка каталога](image/11){#fig:011 width=70%}

Отправляем файлы на сервер

![Отправка файлов на сервер](image/12){#fig:012 width=70%}

Ответы на контрольные вопросы:
1.Что такое системы контроля версий (VCS) и для решения каких задач они
предназначены?
Системы контроля версий (Version Control Systems, VCS) — это инструменты,
позволяющие отслеживать изменения в коде, документации или любых других файлах,
управлять разными версиями проекта и работать в команде без потери данных.
Основные задачи:
• Хранение истории изменений файлов
• Возможность отката к предыдущ
• Разрешение конфликтов при совместной работе
• Управление параллельной разработкой (ветвление и слияние)
• Обеспечение резервного копирования
2.Объяснение понятий VCS и их отношений:
Хранилище (репозиторий) — это база данных, содержащая все файлы проекта и
историю их изменений. Может быть локальным или удалённым.
Commit — фиксация изменений в репозитории. Каждый коммит содержит снимокизменённых файлов и метаданные (автор, дата, комментарий).
История — последовательность коммитов, отображающая все изменения в проекте с
момента его создания.
Рабочая копия — текущая версия проекта на локальном компьютере разработчика,
которая может содержать несохранённые изменения.
3.Централизованные и децентрализованные VCS:
Централизованные VCS (CVCS) используют единый центральный сервер для
хранения всех версий файлов. Разработчики работают с рабочими копиями и получают
обновления с сервера.
Примеры: SVN (Subversion), Perforce, CVS
Децентрализованные VCS (DVCS) — каждый разработчик имеет полную копию
репозитория, включая всю историю изменений. Работа возможна без подключения к
серверу.
Примеры: Git, Mercurial, Fossil
4.Действия при единоличной работе с хранилищем (Git):
Создание репозитория: git init
Добавление файлов: git add <файл>
Фиксация изменений: git commit -m "Описание изменений"
Просмотр истории: git log
Откат к предыдущей версии: git checkout <commit_hash>
Создание веток и переключение между ними: git branch / git checkout
5.Порядок работы с общим хранилищем (Git + удалённый репозиторий):
Клонирование репозитория: git clone <URL>
Создание новой ветки: git checkout -b feature_branch
Добавление изменений: git add .
Фиксация изменений: git commit -m "Описание изменений"
Отправка изменений в удалённый репозиторий: git push origin feature_branch
Обновление локальной версии: git pull
Слияние изменений: git merge feature_branch
6.Основные задачи, решаемые Git:
Отслеживание изменений в файлах
Ведение параллельных разработок с помощьюСлияние и разрешение конфликтов
Работа с локальными и удалёнными репозиториями
Откат к предыдущим версиям проекта
7.Основные команды Git и их краткая характеристика:
git init – создание нового локального репозитория
git clone <URL> – клонирование удалённого репозитория
git add <файл> – добавление файлов в индекс для следующего commit
git commit -m "сообщение" – создание commit'а
git status – проверка состояния репозитория
git log – просмотр истории commit'ов
git branch – просмотр и создание веток
git checkout <ветка> – переключение на другую ветку
git merge <ветка> – слияние веток
git push – отправка изменений в удалённый репозиторий
git pull – получение изменений из удалённого репозитория
git rebase – переписывание истории commit'
git stash – временное сохранение изменений без commit
8.Примеры использования Git с локальными и удалёнными репозиториями:
Локальная работа:
git init
git add .
git commit -m "Первый коммит"
Работа с удалённым репозиторием:
git clone https://github.com/user/repo.git
git pull origin main
git push origin main
9.Что такое ветви (branches) и зач
Ветви позволяют разрабатывать новые функции и исправлять ошибки параллельно, не
изменяя основную версию кода. После завершения работы изменения объединяются с
основной веткой (обычно main или master).
Пример создания и объединения ветки:git checkout -b new-feature
работа с кодом...
git commit -am "Добавлена новая фича"
git checkout main
git merge new-feature
git branch -d new-feature
10. Как и зачем игнорировать файлы при commit?
Некоторые файлы (например, логи, кэш, временные файлы, конфиденциальные
данные) не должны попадать в репозиторий. Для их игнорирования используется
файл .gitignore.
Пример .gitignore:
*.log
node_modules/
.env
Файл .gitignore предотвращает случайное добавление нежелательных файлов в
репозиторий.


# Выводы

Мы изучили идеологию и применение средств контроля версий.
Освоили умения по работе с git.

# Список литературы{.unnumbered}

::: {#refs}
:::
