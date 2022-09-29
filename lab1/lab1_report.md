University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Network programming](https://github.com/itmo-ict-faculty/network-programming)  
Year: 2022/2023  
Group: K34202  
Author: Filippov Artem Alekseevich  
Lab: Lab1  
Date of create: 24.09.2022  
Date of finished: ...  

Цель:  развернуть виртуальную машины на базе платформы Microsoft Azure с установленной системой контроля конфигураций Ansible, установить CHR в VirtualBox и организовать VPN туннель между ними.  

Ход работы:  

1.	Создана виртуальная машина на Yandex Cloud и проведена первичная конфигурация системы для проведения лабораторной работы.  
![Image text](https://https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab1/images/1.png)  
2.	На виртуальную машину установлены python3 и Ansible.    
![Image text](https://https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab1/images/2.png)  
3.	Создана виртуальная машина CHR в VirtualBox.  
![Image text](https://https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab1/images/3.png)  
4.	Для VPN туннеля выбран Wireguard, потому что в беседе написали, что он не работает. На удаленной виртуальной машине установлен Wireguard и осуществлена первичная настройка.  
![Image text](https://https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab1/images/4.png)  
![Image text](https://https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab1/images/5.png)  
5.	Выполнена первичная настройка Wireguard на CHR машине.  
![Image text](https://https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab1/images/6.png)  
![Image text](https://https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab1/images/7.png)  
6.	Добавил публичный ключ CHR клиента в конфиг Wireguard на удаленной виртуальной машине и активировал сервис, после чего пропинговал из CHR удаленную машину по внутреннему Ip туннеля, для того чтобы Wireguard клиент начал отправлять keepalive пакеты для поддержки существования туннеля, ведь клиент у нас за NAT.  
![Image text](https://https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab1/images/8.png)  
![Image text](https://https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab1/images/9.png)  
![Image text](https://https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab1/images/10.png)  
7.	Осуществлена проверка существования туннеля между машинами.  
![Image text](https://https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab1/images/11.png)  
Вывод:  
В ходе выполнения лабораторной работы были созданы две виртуальные машины, одна на Ubuntu другая на CHR. После чего между ними был создан VPN туннель с использованием Wireguard. Все отлично работает.  
