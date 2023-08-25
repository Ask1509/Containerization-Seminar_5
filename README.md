# Контейнеризация (семинары)


## Урок 5. Docker Compose и Docker Swarm


### **Информация о проекте**

Задание:
1) создать сервис, состоящий из 2 различных контейнеров: 1 - веб, 2 - БД
2) далее необходимо создать 3 сервиса в каждом окружении (dev, prod, lab)
3) по итогу на каждой ноде должно быть по 2 работающих контейнера
4) выводы зафиксировать




**Выполнение**

**Термины**

Для того чтобы пользоваться swarm, надо запомнить несколько типов сущностей:

Node - это наши виртуальные машины, на которых установлен docker. Есть manager и workers ноды. Manager нода управляет 
workers нодами. Она отвечает за создание/обновление/удаление сервисов на workers, а также за их масштабирование и 
поддержку в требуемом состоянии. Workers ноды используются только для выполнения поставленных задач и не могут управлять 
кластером.

Stack - это набор сервисов, которые логически связаны между собой. По сути это набор сервисов, которые мы описываем в 
обычном compose файле. Части stack (services) могут располагаться как на одной ноде, так и на разных.

Service - это как раз то, из чего состоит stack. Service является описанием того, какие контейнеры будут создаваться. 
Если вы пользовались docker-compose.yaml, то уже знакомы с этой сущностью. Кроме стандартных полей docker в режиме swarm 
поддерживает ряд дополнительных, большинство из которых находятся внутри секции deploy.

Task - это непосредственно созданный контейнер, который docker создал на основе той информации, которую мы указали при 
описании service. Swarm будет следить за состоянием контейнера и при необходимости его перезапускать или перемещать на 
другую ноду.

![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_1.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_2.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_3.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_4.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_5.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_6.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_7.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_8.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_9.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_10.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_11.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_12.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_13.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_14.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_15.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_16.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_17.png)
![command for linux containerization](https://github.com/Ask1509/Containerization-Seminar_5/blob/main/source/Screenshot_18.png)




