 ##Домашнее задание к занятию 10.4 «Резервное копирование» Андрей Дёмин

### Задание 1

В чём разница между:

- полным резервным копированием,
- дифференциальным резервным копированием,
- инкрементным резервным копированием.

*Приведите ответ в свободной форме.*

<ins>Полное</ins> – это резервное копирование, при котором снимок операционной системы, диска, раздела или отдельных папок содержит все резервируемые данные. Такие снимки, создаваемые в рамках одной и той же задачи по бэкапу, независимы друг от друга, повреждение одного из них никак не повлияет на другие снимки. Это самый надёжный метод резервного копирования, но, вместе с тем, самый затратный по ресурсам дискового пространства.

<ins>Инкрементное</ins> – это такое резервное копирование, при котором полная копия создаётся единожды в начале, а все последующие копии, создаваемые в рамках одной и той же задачи, содержат не все данные, а лишь произошедшие изменения - какие файлы удалены, а какие добавлены. Первая инкрементная копия содержит разницу в данных между ней самой и полной копией. А вторая инкрементная копия содержит разницу между ней самой и первой инкрементной копией. Каждая новая инкрементная копия зависит от предшествующей и не может быть задействована для процесса восстановления без нее  и без полной первичной копии. Каждая из резервных копий задачи представляет собой точку восстановления. И мы всегда сможем выбрать дату или время, на которое хотим откатить систему или данные. Удаление инкрементной копии (или повреждение её вирусами) будет иметь следствием неработоспособность последующих инкрементных копий. 

<ins>Дифференциальное</ins> – это такое резервное копирование, при котором полная копия создаётся единожды в начале, а все последующие копии, создаваемые в рамках одной и той же задачи, содержат все произошедшие изменения с момента создания первичной полной копии. Все следующие дифференциальные копии будут зависимыми только от полной копии. Удаление или повреждение любой из дифференциальных копий не повлияет на другие копии – ни на те, что создавались до удалённой (повреждённой), ни на те, что после неё.
Дифференциальные резервные копии – это тоже точки восстановления. Необходимость дифференциальной копии каждый раз сравнивать себя с полной первичной копией, соответственно, влечёт за собой использование большего дискового пространства. 

---

### Задание 2

Установите программное обеспечении Bacula, настройте bacula-dir, bacula-sd,  bacula-fd. Протестируйте работу сервисов.

*Пришлите конфигурационные файлы для bacula-dir, bacula-sd,  bacula-fd.*

![](img/2-1.png)
![](img/2-2.png)
![](img/2-3.png)
![](img/2-3-1.png)
![](img/2-3-2.png)
![](img/2-3-3.png)
![](img/2-3-4.png)
![](img/2-3-5.png)
![](img/2-4.png)
![](img/2-5.png)
![](img/2-6.png)
![](img/2-7.png)
![](img/2-8.png)
![](img/2-9.png)
![](img/2-10.png)

---

### Задание 3

Установите программное обеспечении Rsync. Настройте синхронизацию на двух нодах. Протестируйте работу сервиса.

*Пришлите рабочую конфигурацию сервера и клиента Rsync.*

![](img/3-1.png)
![](img/3-2.png)
![](img/3-3.png)
![](img/3-4.png)
![](img/3-5.png)
![](img/3-6.png)
