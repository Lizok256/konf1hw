# Задание №1
Разработать эмулятор для языка оболочки ОС. Необходимо сделать работу
эмулятора как можно более похожей на сеанс shell в UNIX-подобной ОС.

Эмулятор должен запускаться из реальной командной строки, а файл с
виртуальной файловой системой не нужно распаковывать у пользователя.

Эмулятор принимает образ виртуальной файловой системы в виде файла формата
tar. Эмулятор должен работать в режиме CLI.

Конфигурационный файл имеет формат ini и содержит:
* Имя компьютера для показа в приглашении к вводу.
* Путь к архиву виртуальной файловой системы.
* Путь к лог-файлу.
* Путь к стартовому скрипту.
  
Лог-файл имеет формат xml и содержит все действия во время последнего
сеанса работы с эмулятором.

Стартовый скрипт служит для начального выполнения заданного списка
команд из файла.

Необходимо поддержать в эмуляторе команды ls, cd и exit, а также
следующие команды:

1. rmdir.
2. du.
3. clear.


# Запуск

Перед запуском необходимо клонировать репозиторий в среду разработки:

```git clone https://github.com/Lizok256/konf1hw```

Запуск emulator.py:

`python3 emulator.py`

Запуск тестов

`python3 tests.p`

# Команды

ls <path> - Список файлов и директорий

cd <path> - Смена директории

exit - Выход из эмулятора

rmdir <path> - Удаление каталога из файловой системы

du <path> - Оценка занимаемого файлового пространства.

clear - Очистка экрана терминала

# Тесты
ls

![](images/ls.png)


cd

![](images/cd.png)


rmdir 

![](images/rmdir.png)

du 

![](images/du.png)


# Общие тесты через pytest

![](images/tests.png)