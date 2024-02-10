# Домашнее задание к занятию «Disaster Recovery. FHRP и Keepalived» - Файзиев Давлат.

### Задание 1
- Дана [схема](https://github.com/netology-code/sflt-homeworks/tree/main/1/hsrp_advanced.pkt) для Cisco Packet Tracer, рассматриваемая в лекции.
- На данной схеме уже настроено отслеживание интерфейсов маршрутизаторов Gi0/1 (для нулевой группы)
- Необходимо аналогично настроить отслеживание состояния интерфейсов Gi0/0 (для первой группы).
- Для проверки корректности настройки, разорвите один из кабелей между одним из маршрутизаторов и Switch0 и запустите ping между PC0 и Server0.
- На проверку отправьте получившуюся схему в формате pkt и скриншот, где виден процесс настройки маршрутизатора.

---
 
### Решение 1
[Cхемa](files/1/hsrp_advanced.pkt) в формате pkt.
  
Cкриншоты настройки маршрутизаторов:
  
![Скриншот 1](img/1_1.png)
  
![Скриншот 2](img/1_2.png)

---
 
### Задание 2
- Запустите две виртуальные машины Linux, установите и настройте сервис Keepalived как в лекции, используя пример конфигурационного [файла](https://github.com/netology-code/sflt-homeworks/blob/main/1/keepalived-simple.conf).
- Настройте любой веб-сервер (например, nginx или simple python server) на двух виртуальных машинах
- Напишите Bash-скрипт, который будет проверять доступность порта данного веб-сервера и существование файла index.html в root-директории данного веб-сервера.
- Настройте Keepalived так, чтобы он запускал данный скрипт каждые 3 секунды и переносил виртуальный IP на другой сервер, если bash-скрипт завершался с кодом, отличным от нуля (то есть порт веб-сервера был недоступен или отсутствовал index.html). Используйте для этого секцию vrrp_script
- На проверку отправьте получившейся bash-скрипт и конфигурационный файл keepalived, а также скриншот с демонстрацией переезда плавающего ip на другой сервер в случае недоступности порта или файла index.html

---

### Решение 2
[Файл bash скрипта](files/2/port-page-check.sh)
  
[Файл keepalived.conf](files/2/keepalived.conf)
  
Скриншоты с демонстрацией переезда плавающего ip на другой сервер в случае недоступности порта или файла index.html:
  
![Скриншот 3](img/2_1.png)
  
![Скриншот 4](img/2_2.png)
  
![Скриншот 5](img/2_3.png)
  
![Скриншот 6](img/2_4.png)

---
