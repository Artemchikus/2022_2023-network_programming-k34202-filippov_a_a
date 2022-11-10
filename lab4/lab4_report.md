University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Network programming](https://github.com/itmo-ict-faculty/network-programming)  
Year: 2022/2023  
Group: K34202  
Author: Filippov Artem Alekseevich  
Lab: Lab4  
Date of create: 06.11.2022  
Date of finished: ...  

Цель:  Изучить синтаксис языка программирования P4 и выполнить 2 задания обучающих задания от Open network foundation для ознакомления на практике с P4.  

Ход работы:  

1.	С помощью Vagrant создана ВМ P4 Tutorial Release 2022-10-31. 
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/1.png)  
2.	Выполнена превичная конфигурация сети "Basic Forwarding" с помощью Makefile, а также проверена связь хостов через Ping.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/2.png)   
3.	Отредактирован файл basic.p4 для правильной кофигурации сети.  
3.1. Добавлен парсинг ethernet и ipv4 headers.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/3.png)  
3.2. Добавлена логика пеерсылки ipv4 пакетов.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/4.png)  
3.3. Добавлена валидация пакетов.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/5.png)  
3.4. Добавлен депарсинг ethernet и ipv4 headers.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/6.png)  
4.	Заново сконфигурирована сеть с помошью Makefile и исправленного basic.p4, проверена связь хостов через Ping и Pingall.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/7.png)    
5.	Отредактирован файл basic_tunnel.p4 для правильной кофигурации сети "Basic Tunneling".  
5.1. Добавлен парсинг myTunnel headers.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/8.png)  
5.2. Добавлена логика пересылки myTunnel пакетов, таблица myTunnel_exact для связи логики пересылки и header dst_id и валидация пактов с учетом myTunnel header.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/9.png)  
5.3. Добавлен депарсинг myTunnel headers.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/10.png)   
6. Заново сконфигурирована сеть с помошью Makefile и исправленного basic_tunnel.p4, проверена связь хостов через Ping и Pingall.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/11.png)   
7. Проверена работа сети через программы receive.py и send.py хостов, а также работа туннелирования, используя параметр dst_id.  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/12.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/13.png)  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/14.png)  
8. Схемы сетей, создаваемых для выполнения заданий:  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/15.png "Implementing Basic Forwarding")  
![Image text](https://github.com/Artemchikus/2022_2023-network_programming-k34202-filippov_a_a/raw/main/lab4/images/16.png " Implementing Basic Tunneling")  
Вывод:  
В ходе выполнения лабораторной работы была создана виртуальная машина для работы с P4. После чего был зучен синтаксис языка программирования P4 и выполнены 2 задания обучающих задания от Open network foundation для ознакомления на практике с P4.  