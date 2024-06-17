# Работа с git и bash
1. Задача 1:
- Открыть домашнюю директорию через терминал  
$ cd  
- Определить имя папки, в которой вы находитесь  
dovga@DESKTOP-KALEHOB MINGW64 ~
$ pwd
/c/Users/dovga
- Создать внутри этой папки каталог с именем test1  
$ mkdir test1  
- Перейти в папку test1  
$ cd test1  
- Создать файл 1,2 и 3 внутри каталога test1  
dovga@DESKTOP-KALEHOB MINGW64 ~/test1  
$ touch 1.txt 2.txt 3.txt
- Проверить содержимое каталога test1  
$ ls  
1.txt  2.txt  3.txt
- Перейти в домашнюю директорию  
$ cd
- Создать папку test2 внутри домашней директории  
dovga@DESKTOP-KALEHOB MINGW64 ~  
$ mkdir test2
- Удалить папку test2  
$ rmdir test2
- Удалить файл 2 из папки test1  
$ cd test1
dovga@DESKTOP-KALEHOB MINGW64 ~/test1       
$ rm 2.txt
- Создать папку в домашней директории test3 и добавить в нее два файла  
$ cd  
dovga@DESKTOP-KALEHOB MINGW64 ~  
$ mkdir test3  
$ cd test3  
dovga@DESKTOP-KALEHOB MINGW64 ~/test3  
$ touch first.txt second.txt  
- Удалить папку test3  
$ cd  
dovga@DESKTOP-KALEHOB MINGW64 ~  
$ rm -r test3
- Создать папку test4 в домашней директории  
$ mkdir test4
- Переместить файлы 1 и 3 из папки test1 в папку test4  
$  cd /c/Users/dovga/test1    
dovga@DESKTOP-KALEHOB MINGW64 ~/test1    
$ mv 1.txt 3.txt /c/Users/dovga/test4
- Добавить в файл 1 три строки со словами line  
$ cd /c/Users/dovga/test4  
dovga@DESKTOP-KALEHOB MINGW64 ~/test4  
$ nano 1.txt
![image](https://github.com/VikaDov/git_bash/assets/118528449/e9f23e78-fe6b-4a09-99cc-f30c3b9b06d8)
- Посмотреть содержимое файла 1  
$ cat 1.txt  
line  
line  
line
- Добавьте в файл 3 три строки со словами line  
$ nano 3.txt
![image](https://github.com/VikaDov/git_bash/assets/118528449/8362b598-584e-40c5-b3b8-8ad997922f9b)
- Просмотрите содержимое двух файлов (1 и 3) сразу  
$ cat 1.txt 3.txt  
line  
line  
line  
line  
line  
line
- Используя один из редакторов замените все строки в файле 1  
vim 1.txt
![image](https://github.com/VikaDov/git_bash/assets/118528449/be3fe7ce-2958-4b23-8664-8fa40cb25b64)
- Проверим, что изменения внеслись   
$ cat 1.txt  
hello  
hello  
hello

3. Задача 2:
- Зайти в домашнюю директорию через терминал.

- Создать папку test 3  

- Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4  

- Найдите строку row2 в файле 5  

- Найдите строку row в папке test3  

- Посчитайте сколько строк с содержимым row в файле 6  

- Найдите файл 5 внутри папки test3  

- Используя команду find, удалите файл 5  

- Используя команду echo, добавьте слово test в файл 4  

- Замените слово test в файле 4 на fail  

- Добавьте в файл 4 слово test так, чтобы сохранилось содержимое  

- Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе  

- Убейте процесс 666 в консоли  

- Узнайте доступность ресурса artsiomrusau.com, используя ping  

- Отправьте 5 пакетов на сайт artsiomrusau.com  

- Используя GET и команду curl, получите информацию о зарегистрированных питомцах на https://petstore.swagger.io/  

- Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/  
