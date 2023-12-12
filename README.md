# Домашнее задание к занятию «Система мониторинга Zabbix. Часть 2»

 ---

### Задание 1
Создайте свой шаблон, в котором будут элементы данных, мониторящие загрузку CPU и RAM хоста.

 ---
 ## Ответ
 
![hw-03zadanie 1](https://github.com/kawahaweto/smon-hw-03/assets/150899286/2d259628-7334-4b0a-a25d-d35bea0aa2fd)

### Задание 2
Добавьте в Zabbix два хоста и задайте им имена <фамилия и инициалы-1> и <фамилия и инициалы-2>. Например: ivanovii-1 и ivanovii-2.

#### Требования к результату
- [ ] Результат данного задания сдавайте вместе с заданием 3

 ---

### Задание 3
Привяжите созданный шаблон к двум хостам. Также привяжите к обоим хостам шаблон Linux by Zabbix Agent.

 ---
## Ответ 
 <details>
 
<summary>Screenshots</summary>

 ![hw-03-23-1](https://github.com/kawahaweto/smon-hw-03/assets/150899286/e77bd404-6116-4ed9-9f0b-f9bd0d6f8f27)

![hw-03-23-02](https://github.com/kawahaweto/smon-hw-03/assets/150899286/cc26ad09-0a0f-4e5e-b853-67ba8950a9b8)

![hw-03-3-3](https://github.com/kawahaweto/smon-hw-03/assets/150899286/62cb4f5a-c206-4506-b5b7-bef652ac5f9f)

 </details>


### Задание 4
Создайте свой кастомный дашборд.

 ---
## Ответ 

![hw-03-4-1](https://github.com/kawahaweto/smon-hw-03/assets/150899286/84732c82-323f-47e5-ab5f-c60b056ab292)

 ---

### Задание 6* со звёздочкой
Создайте UserParameter на bash и прикрепите его к созданному вами ранее шаблону. Он должен вызывать скрипт, который:
- при получении 1 будет возвращать ваши ФИО,
- при получении 2 будет возвращать текущую дату.
 ---
 ## Ответ

 ![image](https://github.com/kawahaweto/smon-hw-03/assets/150899286/7ed67b4e-100d-424c-b977-bb1ed223d0dc)

 <details>

<summary>"Скрипт"</summary>


 ````bash
import datetime
import sys
if (sys.argv[1] == '2'): #
 current_datetime = datetime.datetime.now()
 print(current_datetime)
elif (sys.argv[1] == '1'): #
 print('Barankov A.E.') # 
else: #
 print(f"unknown input: {sys.argv[1]}") #
````

</details>

 ---

