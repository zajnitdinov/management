# Создать репозиторий в системе контроля версий Git (на сайте GitHub) и выполнить базовый набор действий по работе с ним: выполнить операцию commit, создать ветку, выполнить клонирование репозитория, выполнить слияние двух веток. Создание отчета-репозитория о проделанной работе в GitHub, оформление с использованием разметки Markdown.
Создание репозитория в существующем каталоге
## Если у вас уже есть проект в каталоге, который не находится под версионным контролем Git, то для начала нужно перейти в него.

$ cd C:/Users/user/my_project

а затем выполните команду:

$ git init

Эта команда создаёт в текущем каталоге новый подкаталог с именем .git, содержащий все необходимые файлы репозитория — структуру Git репозитория. На этом этапе ваш проект ещё не находится под версионным контролем. Если вы хотите добавить под версионный контроль существующие файлы (в отличие от пустого каталога), вам стоит добавить их в индекс и осуществить первый коммит изменений. Добиться этого вы сможете запустив команду git add несколько раз, указав индексируемые файлы, а затем выполнив git commit:

$ git add *.c
$ git add LICENSE
$ git commit -m 'Initial project version'

## Клонирование существующего репозитория
Для получения копии существующего Git-репозитория, например, проекта, в который вы хотите внести свой вклад, необходимо использовать команду git clone. Клонирование репозитория осуществляется командой git clone . Например, если вы хотите клонировать библиотеку libgit2, вы можете сделать это следующим образом:

$ git clone https://github.com/libgit2/libgit2

Эта команда создаёт каталог libgit2, инициализирует в нём подкаталог .git, скачивает все данные для этого репозитория и извлекает рабочую копию последней версии. Если вы перейдёте в только что созданный каталог libgit2, то увидите в нём файлы проекта, готовые для работы или использования. Для того, чтобы клонировать репозиторий в каталог с именем, отличающимся от libgit2, необходимо указать желаемое имя, как параметр командной строки:

$ git clone https://github.com/libgit2/libgit2 mylibgit

Эта команда делает всё то же самое, что и предыдущая, только результирующий каталог будет назван mylibgit. Когда вы ранее использовали git commit для коммита первоначальной версии в репозиторий, вы включили метку -m, которая делает комментарий в командной строке. Команда commit позволит вам интерактивно редактировать комментарии для коммита. За создание новых веток и слияние их воедино отвечает несколько Git команд.

Git branch
Команда git branch — это своего рода "менеджер веток". Она умеет перечислять ваши ветки, создавать новые, удалять и переименовывать их.

Git merge
Команда git merge используется для слияния одной или нескольких веток в текущую. Затем она устанавливает указатель текущей ветки на результирующий коммит.
