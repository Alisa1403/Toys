
Автор проекта:

Сярибжанова Алиса

## Linux

Используйте команды операционной системы Linux и создайте две новых директории – «Игрушки для школьников» и «Игрушки для дошколят»

- mkdir "Игрушки для школьников" "Игрушки для дошколят"

Создайте в директории «Игрушки для школьников» текстовые файлы - «Роботы», «Конструктор», «Настольные игры»

- cd "Игрушки для школьников"

- touch "Роботы" "Конструктор" "Настольные игры"

Создайте в директории «Игрушки для дошколят» текстовые файлы «Мягкие игрушки», «Куклы», «Машинки»

- cd ../"Игрушки для дошколят"

- touch "Мягкие игрушки" "Куклы" "Машинки"

Объединить 2 директории в одну «Имя Игрушки»

- cd ..

- mv "Игрушки для дошколят" "Имя Игрушки"

- mv "Игрушки для школьников"/* "Имя Игрушки"

- rm -r "Игрушки для школьников"

Переименовать директорию «Имя Игрушки» в «Игрушки»

- mv "Имя Игрушки" "Игрушки"

Просмотреть содержимое каталога «Игрушки».

- ls -la "Игрушки"

total 8

drwxrwxr-x 2 db db 4096 Feb 28 21:45  .

drwxrwxr-x 3 db db 4096 Feb 28 21:49  ..

-rw-rw-r-- 1 db db    0 Feb 28 14:15  Конструктор

-rw-rw-r-- 1 db db    0 Feb 28 21:00  Куклы

-rw-rw-r-- 1 db db    0 Feb 28 21:00  Машинки

-rw-rw-r-- 1 db db    0 Feb 28 21:00 'Мягкие игрушки'

-rw-rw-r-- 1 db db    0 Feb 28 14:15 'Настольные игры'

-rw-rw-r-- 1 db db    0 Feb 28 14:15  Роботы


7.Установить и удалить snap-пакет. (Любой, какой хотите)

- snap search whatsapp

Name                       Version          Publisher        Notes  Summary

whatsapp-app               1.0.1            foksord          -      WhatsApp App

whatsapp-for-linux         1.6.0            nshecan          -      An unofficial WhatsApp desktop application for Linux

whatsapp-4linux            1.1.0            chimekkoo        -      WhatsApp unofficial desktop app for linux

opera                      95.0.4635.46     opera-software✓  -      Fast, secure, easy-to-use browser

ultimate-media-downloader  4.4              keshavnrj✪       -      Online video & audio downloader for Linux, 1300+ websites support

whatsdesk                  0.3.8            zerkc            -      whatsdesk

opera-beta                 96.0.4693.16     opera-software✓  -      Fast and secure web browser

opera-developer            97.0.4704.0      opera-software✓  -      Fast and secure web browser

whatsie                    v4.12.1.fa5add0  keshavnrj✪       -      Feature rich WhatsApp Client for Linux Desktop

kesty-whatsapp             1.2.6            olubunmi708      -      kesty-whatsapp

walc                       0.2.1            cstayyab         -      WALC - unofficial WhatsApp Linux Client

wrapup                     0.1.3            validatedev      -      A Whatsapp client for Linux

whatee                     1.0.0            heliherreradev   -      A simple unofficial WhatsApp desktop client.

singlebox                  29.0.2           webcatalog       -      All-in-One Messenger

cantara                    2.4.1            archchem         -      A Song Presentation Software

ferdi                      5.8.1            getferdi         -      Ferdi

txtme                      2.2.1            txtme            -      txt.me - Customer Service Live Chat


- sudo snap install whatsapp-app

whatsapp-app 1.0.1 from Fatih YOLCU (foksord) installed

- sudo snap remove whatsapp-app

whatsapp-app removed


Добавить произвольную задачу для выполнения каждые 3 минуты (Например, запись в текстовый файл чего-то или копирование из каталога А в каталог Б).

- crontab -e

no crontab for db - using an empty one


Select an editor.  To change later, run 'select-editor'.

1. /bin/nano        <---- easiest

2. /usr/bin/mcedit

3. /usr/bin/vim.tiny

4. /bin/ed

Choose 1-4 [1]: 1

crontab: installing new crontab

crontab -l | grep -v ^#

*/3 * * * * cp -R ~/gb ~/gb_backup




## Приложение магазин игрушек (Java)

Описание

Консольное приложение Магазин игрушек содержит функционал для розыгрыша игрушек. 
Список игрушек, участвующих в розыгрыше содержится в файле toys.csv. 
Розыгранные игрушки записываются в файл out.txt. 

*В программе реализованы следующие функции:*

- просмотр списка игрушек, участвующих в розыгрыше
- просмотр информации по конкретной игрушке
- добавление/изменение/удаление игрушек
- розыгрыш игрушки и добавление её в файл out.txt
- проведение 10-ти розыгрышей подряд и запись информации в файл out.txt
- очистка файла out.txt
- Запуск приложения осуществляется через файл toys/src/Main.java

Управление приложением

Управление приложением осуществляется посредством ввода команд.

Список команд:

- Help - вывод справки по доступным командам
- List - вывод списка всех игрушек
- Read - вывод информации об игрушке по id
- Put - добавление новой игрушки
- Edit - редактирование информации об игрушке по id
- Delete - удаление игрушки по id
- Get - проведение розыгрыша одной игрушки и запись информации в файл out.txt
- Get10 - проведение розыгрыша 10-ти игрушек и запись информации в файл out.txt
- Clear - очистка файла out.txt
- Exit - выход из программы