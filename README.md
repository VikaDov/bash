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
$ rm -rf test3
- Создать папку test4 в домашней директории  
$ mkdir test4
- Переместить файлы 1 и 3 из папки test1 в папку test4  
$  cd test1    
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
$ cd
- Создать папку test3    
dovga@DESKTOP-KALEHOB MINGW64 ~  
$ mkdir test3
- Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4 (добавила вручную)    
$ cd test3  
dovga@DESKTOP-KALEHOB MINGW64 ~/test3
- Найдите строку row2 в файле 5    
$ grep "row2" 5.txt  
row2
- Найдите строку row в папке test3    
$ grep -R "row" .  
./4.txt:row1  
./4.txt:row2  
./4.txt:row3  
./4.txt:row4  
./5.txt:row1  
./5.txt:row2  
./5.txt:row3  
./5.txt:row4  
./6.txt:row1  
./6.txt:row2  
./6.txt:row3  
./6.txt:row4  
- Посчитайте сколько строк с содержимым row в файле 6    
$ grep -c "row" 6.txt  
4
- Найдите файл 5 внутри папки test3  
$ find -name "5.txt"  
./5.txt
- Используя команду find, удалите файл 5  
$ find "5.txt" -delete
- Используя команду echo, добавьте слово test в файл 4  
$ echo test > 4.txt
- Замените слово test в файле 4 на fail  
$ sed -i 's/test/fail/g' 4.txt
- Добавьте в файл 4 слово test так, чтобы сохранилось содержимое  
$ echo "test" | tee -a 4.txt  
test
- Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе  
$ ps aux
- Убейте процесс 666 в консоли  
$ sudo kill 666
- Узнайте доступность ресурса artsiomrusau.com, используя ping  
$ ping artsiomrusau.com  
Обмен пакетами с artsiomrusau.com [15.197.142.173] с 32 байтами данных:  
Ответ от 15.197.142.173: число байт=32 время=12мс TTL=246  
Ответ от 15.197.142.173: число байт=32 время=10мс TTL=246  
Ответ от 15.197.142.173: число байт=32 время=9мс TTL=246  
Ответ от 15.197.142.173: число байт=32 время=8мс TTL=246  
Статистика Ping для 15.197.142.173:  
    Пакетов: отправлено = 4, получено = 4, потеряно = 0  
    (0% потерь)  
Приблизительное время приема-передачи в мс:  
    Минимальное = 8мсек, Максимальное = 12 мсек, Среднее = 9 мсек  
- Отправьте 5 пакетов на сайт artsiomrusau.com  
$ ping -c 5 artsiomrusau.com
- Используя GET и команду curl, получите информацию о зарегистрированных питомцах на https://petstore.swagger.io/  
$ curl https://petstore.swagger.io/v2/pet/findByStatus?status=available
- Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/  
$ curl -X POST https://petstore.swagger.io/v2/user --data "id=60" --data "username=viva" 
--data "firstname=lora" --data "lastname=ivanova" --data "email=testtt@mail.ru" --data "password=loralora" --data "phone=987654321" --data "userStatus=0"  
- Другой вариант создания пользователя
![image](https://github.com/VikaDov/git_bash/assets/118528449/6914d663-9dbb-4b37-843d-54a535aabc7f)


