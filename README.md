# Никоноров Денис - FOPS-8

# Домашнее задание к занятию «Базовые объекты K8S»

### Цель задания

В тестовой среде для работы с Kubernetes, установленной в предыдущем ДЗ, необходимо развернуть Pod с приложением и подключиться к нему со своего локального компьютера. 


### Задание 1. Создать Pod с именем hello-world

1. Создать манифест (yaml-конфигурацию) Pod.

2. Использовать image - gcr.io/kubernetes-e2e-test-images/echoserver:2.2.


Создан манифест [hello-world.yml](/hello-world.yml)

![alt text](img/1.png)

![alt text](img/2.png)

3. Подключиться локально к Pod с помощью `kubectl port-forward` и вывести значение (curl или в браузере).

![alt text](img/3.png)

С помощью curl проверен ответ от пода на GET-запрос

![alt text](img/4.png)
------

### Задание 2. Создать Service и подключить его к Pod

1. Создать Pod с именем netology-web.
2. Использовать image — gcr.io/kubernetes-e2e-test-images/echoserver:2.2.
3. Создать Service с именем netology-svc и подключить к netology-web.

Создан манифест [service.yml](/service.yml) объединён под с серивисом.

![alt text](img/5.png)

Запуск пода и сервиса 

![alt text](img/6.png)

Подключение к сервису с `kubectl port-forward`

![alt text](img/7.png)

4. Подключиться локально к Service с помощью `kubectl port-forward` и вывести значение (curl или в браузере).

![alt text](img/8.png)

------