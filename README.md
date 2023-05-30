# Информация о проекте

Необходимо организовать систему учета для питомника, в котором живут
домашние и вьючные животные.

### Задание

<a href="resources/files/Итоговая%20аттестация.pdf" target="_blank">Файл задания</a>

1. Используя команду cat в терминале операционной системы Linux, создать два файла *Домашние животные* (заполнив файл собаками, кошками, хомяками) и *Вьючные животными* заполнив файл (Лошадьми, верблюдами и ослы), а затем объединить их. 
Просмотреть содержимое созданного файла. Переименовать файл, дав ему новое имя (Друзья человека).

```bash
cat > Домашние_животные
```

```
кошка
собака
хомяк
попугай
```

```bash
cat > Вьючные_животные
```

```
лошадь
верблюд
осел
мул
```

``` bash
ls
cat Домашние_животные
cat Вьючные_животные
cat Домашние_животные Вьючные_животные > Животные
ls
cat Животные
mv Животные Друзья_человека
ls
```

![Task1](./resources/image/task1.png)

2. Создать директорию, переместить файл туда.

```
sudo mkdir Животный_мир
ls
sudo mv Друзья_человека Животный_мир/
ls
ls Животный_мир/*
```


![Task2](./resources/image/task2.png)

3. Подключить дополнительный репозиторий MySQL. Установить любой пакет из этого репозитория.
```bash
sudo wget -c https://dev.mysql.com/get/mysql-apt-config_0.8.25-1_all.deb
sudo dpkg -i mysql-apt-config_0.8.25-1_all.deb
sudo apt install mysql-client -y
```

![Task3](./resources/image/task3.png)

4. Установить и удалить deb-пакет с помощью dpkg.

```bash
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome-stable_current_amd64.deb
sudo dpkg -r google-chrome-stable
```

![Task4](./resources/image/task4.png)

5. Выложить историю команд в терминале ubuntu
```bash
history > TerminalHistory.txt
```

<a href="resources/files/TerminalHistory.txt" target="_blank">TerminalHistory.txt</a>

6. Нарисовать [диаграмму](./resources/diagramm/UML.drawio), в которой есть класс родительский класс, домашние животные и вьючные животные, в составы которых в случае домашних животных войдут классы: собаки, кошки, хомяки, 
а в класс вьючные животные войдут: (Лошади, верблюды и ослы).


![Task6](./resources/image/task6.png)

7. В подключенном MySQL репозитории создать базу данных “Друзья человека”

8. Создать таблицы с иерархией из диаграммы в БД

9.  Заполнить низкоуровневые таблицы именами(животных), командами которые они выполняют и датами рождения

10. Удалив из таблицы верблюдов, т.к. верблюдов решили перевезти в другой питомник на зимовку. Объединить таблицы лошади, и ослы в одну таблицу.

11. Создать новую таблицу “молодые животные” в которую попадут все животные старше 1 года, но младше 3 лет и в отдельном столбце с точностью до месяца подсчитать возраст животных в новой таблице

12. Объединить все таблицы в одну, при этом сохраняя поля, указывающие на прошлую принадлежность к старым таблицам.

13. Создать класс с Инкапсуляцией методов и наследованием по диаграмме.

14. Написать программу, имитирующую работу реестра домашних животных. В программе должен быть реализован следующий функционал:
14.1 Завести новое животное
14.2 определять животное в правильный класс
14.3 увидеть список команд, которое выполняет животное
14.4 обучить животное новым командам
14.5 Реализовать навигацию по меню

15. Создайте класс Счетчик, у которого есть метод add(), увеличивающий
значение внутренней int переменной на 1 при нажатии “Завести новое
животное” Сделайте так, чтобы с объектом такого типа можно было работать в
блоке try-with-resources. Нужно бросить исключение, если работа с объектом
типа счетчик была не в ресурсном try и/или ресурс остался открыт. Значение
считать в ресурсе try, если при заведении животного заполнены все поля.