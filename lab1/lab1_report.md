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

![image](https://github.com/user-attachments/assets/beef707f-fc64-49a1-a92f-5bcbf1218211)


### Создан минимальный compute engine (виртуальную машину) с Machine type e2-micro в режиме spot.

![image](https://github.com/user-attachments/assets/0ef97099-deae-4b19-ac8a-d1eba2ab084b)
![image](https://github.com/user-attachments/assets/e4e77cad-65ce-40d5-8c13-84b9b76d612a)
![image](https://github.com/user-attachments/assets/609b3a82-af6f-43ef-9458-29c4430ba7f6)
![image](https://github.com/user-attachments/assets/af869eaa-3edd-4a60-b7d7-9a941808d268)

### С помощью утилиты gsutils найден бакет lab1-bucket-itmo и скопирован 3 файла в локальную папку на VM. 

![image](https://github.com/user-attachments/assets/8ce8d933-e75d-49a9-a239-e46a9c230cf6)

### Проверям, что эти файлы хранятся на VM.

![image](https://github.com/user-attachments/assets/002550c8-c11c-4284-8069-95e4314ed939)

### Права доступа изменены для service account с Storage Admin на Compute Viewer, скопировать файлы не удалось.

![image](https://github.com/user-attachments/assets/310a7fbb-dafe-490d-9bbc-1d1905b9e2f8)

### Вывод:
Роль Storage Admin предоставляет полный контроль над контейнерами, папками, управляемыми папками и объектами.
Compute Viewer дает доступ только для чтения и для получения и просмотра информации обо всех ресурсах Compute Engine, включая экземпляры, диски и брандмауэры. 
Роль Compute Viewer позволяет получать и просматривать информацию о дисках, образах и снимках, но не позволяет читать хранящиеся на них данные.
