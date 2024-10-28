#### University: [ITMO University](https://itmo.ru/ru/)
#### Faculty: [FTMI](https://ftmi.itmo.ru/)
#### Course: Cloud platforms as the basis of technology entrepreneurship
#### Year: 2024/2025
#### Group: U4225
#### Author: Vybornova Alexandra Vladimirovna
#### Lab: Lab2
#### Date of create: 25.10.2024
#### Date of finished: 28.10.2024

## Описание
Это вторая лабораторная работа "Исследование Cloud Run".

## Цель работы
Ознакомиться с работой Cloud Run.

## Ход работы

### Создан Cloud Run из представленного дефолтного сервиса Hello.
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/7a3fd18e-da9b-4fc7-b035-ad096a98d04c">

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/1c73bc32-6c0e-4af3-b596-7d39e27cbcbb">

### Cloud Run запущен.

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/58a51594-ca89-40bf-b4c8-4e5af0e5b20a">


### Логи и метрики:
Логи:
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/46452d8a-e203-4512-acd2-792a5505ac9a">
Сервис успешно запущен
Запросы Get выполняются успешно, время отклика от 4 до 9 ms.

Метрики:
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/79766b35-5a24-43f8-badb-dfc5b1796064">
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/c3827d0c-8f1e-46db-9064-cae2905d109f">
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/b34835a9-1217-4975-9198-128857dac584">

Метрики показывают, что в периоды активности сервис работает стабильно, без значительных пиков нагрузки, с низкими задержками и использованием ресурсов, так как нагрузка минимальна.

### Cloud Run изменен, выбран 8090 порт.

<img width="1440" alt="image" src="https://github.com/user-attachments/assets/f3e48795-eb4f-4c41-a3d3-a40a9977d5c8">
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/453f1d46-aadc-49e6-b4db-4a4770c71957">
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/ed9d797b-0910-4e4a-9123-85afcde49565">

Логи:
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/82e9037b-d8d4-49ee-8bd7-d2a69ee1742c">
Поменяли порт на 8090, запущено удачно. Get запрос - 4 ms. 

Метрики:
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/8c935f97-dd9a-41a9-8d22-ee3adfb6806b">
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/69240bfe-5c44-459b-a6db-27c1199fb6b1">
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/e49dcfa2-27dc-4859-a9f1-31aeb34e03d8">

После смена порт на 8090:
Использование памяти поднялось до 4-5%, что больше на 2-3%, но некритично.

В остальном пики нагрузки также не наблюдаются, нагрузка на низком уровне, с низкими задержками. Сервис работает стабильно.

### Перераспределение трафика.
При перераспределении трафика между портами 50 на 50 следующие метрики:
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/e157485e-e5b2-4733-9e27-d28c31735402">
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/b77df3e7-115b-4e59-a037-8845aa0ecd6e">

При перераспределении трафика между портами 90 на 10 следующие метрики:
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/b7b6a3f7-ac5c-4021-88e8-89e164071f37">
<img width="1439" alt="image" src="https://github.com/user-attachments/assets/d7b44cf6-c534-494d-b3f8-20b9b5902df5">

Снова метрики распределения трафика между портами 50 на 50:
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/acdeaad6-81e7-4dc0-8de5-36ad753d0133">
Мы видим, что использование памяти уменьшилось, задержка запросов тоже уменьшается.

### Вывод:
При перераспределении трафика поровну между двумя портами, нагрузка должна уменьшаться.
