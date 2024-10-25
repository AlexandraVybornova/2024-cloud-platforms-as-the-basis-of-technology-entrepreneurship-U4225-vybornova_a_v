#### University: [ITMO University](https://itmo.ru/ru/)
#### Faculty: [FTMI](https://ftmi.itmo.ru/)
#### Course: Cloud platforms as the basis of technology entrepreneurship
#### Year: 2024/2025
#### Group: U4225
#### Author: Vybornova Alexandra Vladimirovna
#### Lab: Lab1
#### Date of create: 21.10.2024
#### Date of finished: 25.10.2024

## Описание
Это первая лабораторная работа "Обзор Google Cloud и исследование основных сервисов."

## Цель работы
Ознакомиться с основными возможностями и преимуществами облачной платформы Google Cloud.

## Ход работы

### Во вкладке IAM создан service account с ролью Storage Admin.



### Создан минимальный compute engine (виртуальную машину) с Machine type e2-micro в режиме spot.


### С помощью утилиты gsutils найден бакет lab1-bucket-itmo и скопирован 3 файла в локальную папку на VM. 

### Используя команду ls -lah показано, что эти файлы хранятся на VM.

### Права доступа изменены для service account с Storage Admin на Compute Viewer, скопировать файлы не удалось.

### Вывод:
Роль Storage Admin предоставляет полный контроль над контейнерами, папками, управляемыми папками и объектами.
Compute Viewer дает доступ только для чтения и для получения и просмотра информации обо всех ресурсах Compute Engine, включая экземпляры, диски и брандмауэры. 
Роль Compute Viewer позволяет получать и просматривать информацию о дисках, образах и снимках, но не позволяет читать хранящиеся на них данные.
