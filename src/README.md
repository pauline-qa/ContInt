## **Описание счетчиков покрытия JaCoCo**

### INSTRUCTION (C0-покрытие)

Самая маленькая единица измерения JaCoCo - это одиночные инструкции кода байта Java. Покрытие инструкции предоставляет
информацию о количестве кода, который был выполнен или пропущен. Эта метрика полностью независима от исходного
форматирования и всегда доступна даже в отсутствие отладочной информации в файлах классов.

### **BRANCH (C1 Покрытие)**

JaCoCo также вычисляет охват веток для всех операторов if и switch. Эта метрика подсчитывает общее количество таких
ветвей в методе и определяет количество выполненных или пропущенных ветвей. Распространение веток всегда доступно, даже
при отсутствии отладочной информации в файлах классов. 

Если файлы классов были скомпилированы с информацией об отладке, точки принятия решений могут быть сопоставлены с
исходными строками и подсвечены соответственно:

* Нет покрытия: нет ответвлений в линии (красный ромб)
* Частичное покрытие: выполнена только часть ветвей в линии (желтый ромб)
* Полное покрытие: все ответвления в линии выполнены (зеленый ромб)

### **LINE**

Для всех файлов классов, которые были скомпилированы с информацией об отладке, можно рассчитать информацию о покрытии
для отдельных строк. Исходная строка считается выполненной, когда была выполнена хотя бы одна команда, назначенная этой
строке.

В связи с тем, что одна строка обычно компилируется в несколько команд с байтовым кодом, подсветка исходного кода
показывает три разных состояния для каждой строки, содержащей исходный код:

* Нет покрытия: ни одна инструкция в строке не была выполнена (красный фон)
* Частичное покрытие: выполнена только часть инструкции в строке (желтый фон)
* Полное покрытие: все инструкции в строке выполнены (зеленый фон)