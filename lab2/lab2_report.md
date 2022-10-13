University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Network programming](https://github.com/itmo-ict-faculty/network-programming)  
Year: 2022/2023  
Group: K34202  
Author: Filippov Artem Alekseevich  
Lab: Lab2  
Date of create: 09.10.2022  
Date of finished: ...  

Цель:  с помощью Ansible настроить несколько сетевых устройств и собрать информацию о них, а также правильно собрать файл Inventory.  

Ход работы:  

1.	Установлен второй CHR на локальном ПК, и организован второй OVPN Client (Wireguard) на втором CHR.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/1.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/2.png)  
2.	С обоими CHR настроено ssh соединение с помощью ключей для удобной работы Ansible.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/3.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/4.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/5.png)  
3.	Осуществлена первичная настройка Ansible, путем добавления файлов hosts, ansible.cfg и routers.yml. Проверена работа Ansible с помощью test.yml, в ходе которой были скачаны дополнительные Python библиотеки для работы с ssh.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/7.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/8.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/10.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/11.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/12.png)  
4.	Используя Ansible, настроены логин/пароль сразу на 2-х CHR.   
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/13.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/14.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/14.5.png)  
5.	Используя Ansible, настроены NTP-клиенты сразу на 2-х CHR.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/15.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/16.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/17.png)  
6.	Используя Ansible, настроен OSPF роутинг сразу на 2-х CHR.    
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/21.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/19.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/20.png)  
7.	Используя Ansible, собраны данные по OSPF топологии и полный конфиг устройства сразу на 2-х CHR, после чего результаты сохранены в файлах r1.json и r2.json.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/22.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/23.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/24.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/25.png)  
8. Проведены проверки связности с помощью команды ping.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/26.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/27.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/28.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/29.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/30.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/31.png)  
9. Составлена схема сети получившейся сети в draw.io.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab2/images/32.png)  
Вывод:  
В ходе выполнения лабораторной работы был создан еще один CHR. После чего удаленно были проведены различные настройки обоих CHR с помощью Ansible, установленного на удаленной ВМ, находящейся в YandexCloud.  
