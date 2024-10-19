# Работа с git.  

## Команды.  

pwd - Узнать, где вы сейчас, (от англ. — «показать рабочую папку»). Она выводит путь к текущей директории. Это путь к домашней директории

cd ~ - перейти к домашней директории. cd - сменить директорию. Символ ~ обозначение домашней директории.

cd имя_папки - (сменить директорию на ту, что указана после команды cd). Если в названии папки есть пробелы, необходимо использовать кавычки. Так же cd позволяет перемещаться сразу через несколько директорий, в таком случае необходимо разделить их знаком /. Что бы обратиться к текущей директории можно использовать cd . но это нужно довольно редко.

Пример: cd "Фотографии с дня рождения".

ls - вывести содержимое директории (выводит все папки и файлы исходя из директории в который вы сейчас находитесь). С помощью команды ls -a можно вывести все файлы и скрытые.

А ещё, как и другие команды, ls может работать с символом домашней директории (~) и предыдущей директории (..). Например, ls~ выведет содержимое домашней директории вне зависимости от того, что показывает pwd. А ls .. покажет содержимое родительской директории.

touch Имя_файла - создает файл.

А команда touch ../../file.txt создаст файл file.txt на две папки выше по иерархии. Допустим, если вы находитесь в директории projects/git/hello, команда touch ../../file.txt создаст файл по такому пути: projects/file.txt.

mkdir Имя_директории - создает новую директорию.

mkdir -p Имя_директории/Имя_директории/Имя_директории - создаст целую структуру директорий.

Также можно использовать обе команды вместе с символом домашней директории (~) или родительской директории (..). Например, команда mkdir ~/my-git-projects создаст папку my-git-projects внутри домашней директории.

cp что_копируем куда_копируем - какой файл копируем и куда копируем. но можно указать и сразу несколько файлов для копирования.

mv что_перемещаем куда_перемещаем - перемещение (удаляем файл в одном месте, перемещаем в другое). После имени команды указывают список файлов и папок, которые нужно переместить, а затем — папку, в которую нужно выполнить перемещение.

cat - Что бы прочитать файл в консоль необходимо ввести cat, вместе с именем файла. Команда распечатает то, что содержится в нем. Она работает только с текстовыми файлами.

rm - Что бы удалить, нужно напечатать команду rm и передать ей имя файла.

rmdir - удалить папку можно командой rmdir и так же указать имя папки. Если в папке есть файлы, то она не удалится и командная строка выведет сообщение о том, что папка не пуста Directory not empty.

rm -r - если папка не пуста и ее все таки нужно удалить со всем содержимым. Эта команда рекурсивно удаляет файлы и папки. Это значит что удаление будет последовательно применяться к каждому элементу в этой папке.

Эффективная работа с командной строкой.

Выполняйте сразу несколько команд.

Команды в терминале необязательно вбивать и выполнять по очереди. Их можно указывать не по одной, а сразу списком. Для этого их нужно разделить двумя амперсандами (&&).

git init - создает git репозиторий. Для этого следует переместиться в неё и ввести команду git init.

rm -rf .git - что бы удалить папку с репозиторием нужно удалить файл в папке .git, но учитывайте, что если вы удалите папку .git вся информация о репозитории будет стерта и останется только версия с последними изменениями.

git status - проверить состояние репозитория(проверить статус репозитория).

git add или git add --all или git add . - сохранить файлы в гит.

После команды git add пишем имя файла, который хотим сохранить.

Команда git add --all сохраняет все файлы в директории git.

Команда git add . добавляет в репозиторий текущую папку со всеми файлами.

git commit -m "текст_коммита" - сохраняет изменения в репозитории. Когда вы редактируете файлы в проекте, Git отслеживает изменения, но они не считаются окончательными, пока вы не выполните git commit.

Разница между git add и git commit.

Сначала команда git add сообщает Git, какие именно файлы нужно сохранить и какую их версию. Затем с помощью команды git commit происходит само сохранение.

git log - посмотреть историю коммитов.