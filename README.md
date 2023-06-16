# Exceptions_JAVA
### Исключительная ситуация (исключение)     – это событие, которое происходит во время исполнения программы и нарушает нормальную последовательность выполнения команд или инструкций программы.
### Обработка исключения – это создание альтернативного пути исполнения программы.
В Java все исключения описаны через классы, которые связаны в иерархическую структуру. На вершине этой иерархии находится класс `Throwable`, у которого есть два наследника – `Error` и `Exception` – из пакета `java.lang.` Все остальные исключения являются их наследниками.

### Существует две категории исключений:
- проверяемые (checked)
- непроверяемые (unchecked).

#### Unchecked
Непроверяемые исключения делятся на ошибки (errors) и исключения времени исполнения (runtime exception).

Error:
* `AssertionError`	Диагностическая проверка прошла неуспешно
* `InternalError`	Непредвиденная внутренняя ошибка виртуальной машины
* `OutOfMemoryError`	Виртуальная машина не может выделить память под объект
* `StackOverflowError`	Переполнение стека из-за глубокой рекурсии программы
* `ThreadDeath`	Происходит, когда поток вызывает устаревший метод stop()
* `UnknownError`	Происходит неизвестная, но серьезная ошибка виртуальной машины
* `VirtualMachineError`	Происходит, когда виртуальная машина сломана или не хватает ресурсов

Все исключительные ситуации типа `Exception`, кроме семейства `RuntimeException`, относятся к категории проверяемых исключений, то есть такие исключения ожидаемы. Например, класс не найден или ошибка ввода/вывода. Поэтому возникновение такого исключения может быть отслежено еще на этапе компиляции кода, то есть компилятор проверяет, может ли метод бросить исключение. Если может, то компилятор будет требовать указать размещение кода обработки исключения: либо в методе, где оно возникло, либо в другом месте.

У класса Exception есть особый подкласс IOException, который определяет семейство исключений, связанных с операциями ввода/вывода.

Exception:
* `ClassNotFoundException`	Класс не найден
* `CloneNotSupportedException`	Попытка клонировать объект, который не поддерживает операцию клонирования
* `ConnectException`	Попытка подключить сокет к удаленному адресу и порту
* `EOFException`	Когда при чтении неожиданно достигнут конец файла или потока данных
* `IllegalAccessException`	Доступ к классу отклонен
* `InstantiationException`	Попытка создать объект абстрактного класса или интерфейса
* `InterruptedException`	Один поток прерывает другой поток
* `InvalidClassException`	Когда в процессе сериализации возникают проблемы с классом
* `InvalidObjectException`	Когда один или более десериализованных объектов не прошли валидацию
* `IOException`	Общий класс исключений, вызванных неудачными или прерванными операциями ввода-вывода
* `MalformedURLException`	Когда адрес URL некорректный
* `NoSuchFieldException`	Требуемое поле не существует
* `NoSuchMethodException`	Требуемый метод не существует
* `NotSerializableException`	Класс не является сериализуемым
* `ObjectStreamException`	Общий класс для всех исключений с объектными потоками ввода/вывода
* `ReflectiveOperationException`	Общий класс исключений, определяющий ошибки при использовании рефлексии
* `SocketException`	Ошибка создания сокета или доступа к нему
* `UnknownHostException`	IP-адрес хоста не может быть определен

Все исключительные ситуации типа `RuntimeException` относятся к категории непроверяемых исключений. Иначе говоря, они неожидаемые, происходят во время исполнения программы, а компилятор не имеет возможности проверить такие ситуации заранее. Обычно они указывают на логические ошибки программы или неправильное использование API. Например, деление на ноль, выход за границу массива индекса, недопустимое приведение типов.

* RuntimeException:
* `ArithmeticException`	Арифметическая ошибка типа деления на ноль
* `ArrayIndexOutOfBoundsException`	Индекс массива находится вне границ
* `ArrayStoreException`	Сохранение в элементе массива объекта несовместимого типа
* `ClassCastException`	Недопустимое приведение типов
* `IllegalArgumentException`	Методу передан некорректный аргумент
* `IllegalMonitorStateException`	Незаконная операция монитора
* `IllegalStateException`	Среда или приложение находятся в неподходящем состоянии для вызова метода
* `IllegalThreadStateException`	Требуемая операция не совместима с текущим состоянием потока
* `IndexOutOfBoundsException`	Некоторый тип индекса находится вне диапазона
* `NegativeArraySizeException`	Массив создавался с отрицательным размером
* `NullPointerException`	Недопустимое использование нулевой ссылки
* `NumberFormatException`	Попытка преобразовать строку в один из числовых типов, но строка не имеет соответствующего формата.
* `SecurityException`	Попытка нарушить защиту
* `StringIndexOutOfBoundsException`	Индекс символа строки находится вне границ
* `UnsupportedOperationException`	Встретилась неподдерживаемая операция



