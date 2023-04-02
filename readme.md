# Инструкция по работе с git 

## Что такое git

***Git*** - самая популярная реализация распределенной системы контроля версий (версионность поддерживается и на сервере, и у каждого клиента). Самой распространенной реализацией ***Git*** 
является (GitHub)[https://github.com/]

## Подготовка репозитория
Для создания репозитория используется команда *git init*. Для этого необходимо открыть в терминале папку с будущем репозиторием и написать *git init*.

## Создание "сохранений"
для создания новой фиксации используется команда  *git commit*. Для этого в терминале с папкой-репозиторием пишем *git commit -m "<сщщбщение к коммиту>*. Сообщение к коммиту писать ***обязательно ***


### Добавление файлов к коммиту
Для добавления файла к новому коммиту используется команда *git add*. Используется она следующим образом: в терминале с папкой - репозиторием пишем *git add <название файла>*.


## Журнал изменений 
Для просмотра историй изменений используется команда *git log* . Для этого в терминале с папкой-репозиторием необходимо написать *git log*

## Перемещение между коммитами
Для перемещения на другую фиксацию(коммит) используется команда *git checkout*. Для этого необходимо, как показано в прошлом пункте, в журнале изменений найти необходимый коммит и его хеш (номер), после чего в терминале с папкой-репозиторием надо написать *git checkout <хеш коммита>*.

После выполнения этой команды мы попадем в состояние **detached head**, в котором никакие следующие коммиты сохраняться не будут. Для выхода из этого состояния необходимо написать *git checkout master*

## Ветки в гит

Часто над одним файлом работают сразу несколько человек. Чтобы не изменять один и тот же файл **Git** позволяет сделать несколько веток для выполнения каждой задачи. 

Для создания новой ветки необходимо в терминале надо написать *git branch <название ветки>*

Команда *git branch* — это своего рода "менеджер веток". Она умеет перечислять ваши ветки, создавать новые, удалять и переименовывать их.

Команда *git checkout* используется для переключения веток и выгрузки их содержимого в рабочий каталог.

## Слияние веток и разрешение конфликтов

Команда *git merge* используется для слияния одной или нескольких веток в текущую. Затем она устанавливает указатель текущей ветки на результирующий коммит.

Чтобы использовать эту команду нужно перейти на ветку, в которую будет добавлена информация и написать в терминале *git merge <название ветки>*

в некоторых ситуациях могут возникать конфликты между ветками. Их необходимо устранять в ручную. Для этого необходимо в появившемся сообщении выбрать нужное исправление.


## Ветки, которые можно удалить

После слияния вся информация будет находиться в главной ветке, соответственно, ненужную ветку можно удалить. Для этого в терминале пишем *git branch -d <название ветки>*

