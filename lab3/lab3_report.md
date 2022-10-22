University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Network programming](https://github.com/itmo-ict-faculty/network-programming)  
Year: 2022/2023  
Group: K34202  
Author: Filippov Artem Alekseevich  
Lab: Lab3  
Date of create: 22.10.2022  
Date of finished: ...  

Цель:  с помощью Ansible и Netbox собрать всю возможную информацию об устройствах и сохранить их в отдельном файле.  

Ход работы:  

1.	Поднят Netbox на дополнительной VM. 
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab3/images/1.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab3/images/2.png)  
2.	Заполнена вся возможная информация о CHR в Netbox.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab3/images/3.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab3/images/4.png)  
3.	Используя Ansible и роли для Netbox в тестовом режиме все данные из Netbox сохранены в отдельный файл.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab3/images/5.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab3/images/6.png)    
4.	Написан сценарий, при котором на основе данных из Netbox можно настроить 2 CHR, изменить имя устройства, добавить IP адрес на устройство.   
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab3/images/7.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab3/images/8.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab3/images/9.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab3/images/10.png)  
5.	Написан сценарий, позволяющий собрать серийный номер устройства и вносящий серийный номер в Netbox. Так как серицного момера у виртуального CHR нет, то было принято решение использовать License Id.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab3/images/11.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab3/images/12.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab3/images/13.png)   
6. Проведены проверки связности с помощью команды ping.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab3/images/14.png)   
7. Отредкатирована схема сети получившейся сети в draw.io.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab3/images/15.png)  

Вывод:  
В ходе выполнения лабораторной работы была создана виртуальная машина с Netbox. После чего удаленно с помощью Ansible и Netbox были проведены настройки обоих CHR, а также настройка Netbox с помощью информации взятой из CHR.  